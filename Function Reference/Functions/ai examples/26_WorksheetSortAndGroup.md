# 26. Sorting and Grouping with `SetWSColumnOperators`

## Description
Extends the database-row schedule from example 24 by asking the worksheet to
sort ascendingly on one column and total another. This is exactly the pattern
used by the mechanical `CreateBillOfMaterials.px` and `CreatePartsList.px`
scripts to produce grouped, quantity-summed reports.

## What This Demonstrates
- Two-argument sort/summarize control via
  [`SetWSColumnOperators`](../SetWSColumnOperators.md)
- The role of the **database row index** (row 2 in this file) as anchor
  for the operators
- Group-summary rows that Vectorworks folds in automatically once a sort
  operator is set on a column

## Python Script
```python
import vs

kWSName  = 'Furniture by Room'
kRecName = 'Furniture Info'


def cell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def db_criteria(rec):
    return "=DATABASE((R IN ['" + rec + "']))"


def field_ref(rec, field):
    return "=('" + rec + "'.'" + field + "')"


def seed():
    """Attach the record to a handful of rectangles across two rooms."""
    vs.NewField(kRecName, 'AssetTag',   '',    4, 0)
    vs.NewField(kRecName, 'RoomNumber', '101', 4, 0)
    vs.NewField(kRecName, 'Quantity',   '1',   1, 0)

    samples = [
        ('DESK-01',  '101', 1),
        ('DESK-02',  '101', 1),
        ('CHAIR-01', '101', 4),
        ('DESK-03',  '102', 1),
        ('CHAIR-02', '102', 6),
        ('LAMP-01',  '102', 2),
    ]
    for i, (tag, room, qty) in enumerate(samples):
        vs.Rect(i * 1.2, 0, i * 1.2 + 1.0, 0.6)
        h = vs.LNewObj()
        vs.SetRecord(h, kRecName)
        vs.SetRField(h, kRecName, 'AssetTag',   tag)
        vs.SetRField(h, kRecName, 'RoomNumber', room)
        vs.SetRField(h, kRecName, 'Quantity',   str(qty))


def main():
    seed()

    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)
    ws = vs.CreateWS(kWSName, 3, 3)

    cell(ws, 1, 1, 'Asset')
    cell(ws, 1, 2, 'Room')
    cell(ws, 1, 3, 'Qty')

    # Database row at index 2 (column 0 = criteria).
    kDBRow = 2
    vs.SetWSCellFormula(ws, kDBRow, 0, kDBRow, 0, db_criteria(kRecName))
    cell(ws, kDBRow, 1, field_ref(kRecName, 'AssetTag'))
    cell(ws, kDBRow, 2, field_ref(kRecName, 'RoomNumber'))
    cell(ws, kDBRow, 3, field_ref(kRecName, 'Quantity'))

    # Column operators.
    #   sort:  negative = ascending, positive = descending, 0 = none.
    #          Absolute value is the column index (1-based).
    #   sum:   1 = sum, 2 = average, 3 = count, 0 = none.
    #
    #   Here: sort ASC by column 2 (RoomNumber) as sort1,
    #         then ASC by column 1 (AssetTag)  as sort2,
    #         and total column 3 (Qty)         as sum1.
    vs.SetWSColumnOperators(ws, kDBRow, -2, -1, 0, 3, 0, 0)

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message('Grouped schedule created.')


main()
```

## Sort / Summarize Reference
`SetWSColumnOperators(ws, dbRow, sort1, sort2, sort3, sum1, sum2, sum3)`

| Parameter | Meaning                                                          |
|-----------|------------------------------------------------------------------|
| `sortN`   | Column index (signed); negative = ascending, positive = descending, 0 = none |
| `sumN`    | Column index that gets a summary. Value 0 disables. Combine with the row's group-collapse arrow to see totals per group |

Setting even one non-zero `sortN` causes the database to render a grouped
summary row above each block of matching subrows.

## Key Functions
- [`SetWSColumnOperators`](../SetWSColumnOperators.md)
- [`SetWSCellFormula`](../SetWSCellFormula.md), [`NewField`](../NewField.md), [`SetRecord`](../SetRecord.md), [`SetRField`](../SetRField.md)
