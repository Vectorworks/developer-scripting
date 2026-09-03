# 24. Auto-Populating Database Row

## Description
A **database row** is a row in a worksheet whose cell **at column 0** carries
a `=DATABASE((criteria))` formula. Vectorworks automatically inserts one
sub-row per object that matches the criteria; the other cells on that row use
column formulas of the form `=('RecordName'.'FieldName')` to pull values off
each matching object.

This is the technique behind every real schedule in the project
(`Create Panel Schedule.px`, `Property Line.px`, `Create Rm Finish Legend.px`
and the Spotlight cable/hoist worksheets).

## What This Demonstrates
- Attaching a record to a set of test objects so we have something to report
- Creating a **database row** with a criteria formula in column 0
- Column formulas that dereference record fields
- Recalculating so the sub-rows populate

## Python Script
```python
import vs

kWSName  = 'Furniture Schedule'
kRecName = 'Furniture Info'


def cell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def db_criteria(rec_name):
    """Assemble a =DATABASE(...) formula for the given record.

    The awkward doubled single quotes are how you write a Pascal-style
    string literal inside a Pascal-style string.
    """
    return "=DATABASE((R IN ['" + rec_name + "']))"


def field_ref(rec_name, field_name):
    """Assemble the =('Record'.'Field') column formula for a database row."""
    return "=('" + rec_name + "'.'" + field_name + "')"


def seed_test_objects():
    """Drop three rectangles and attach the record with sample values."""
    vs.NewField(kRecName, 'AssetTag',   '',      4, 0)   # 4 = text
    vs.NewField(kRecName, 'RoomNumber', '101',   4, 0)
    vs.NewField(kRecName, 'Quantity',   '1',     1, 0)   # 1 = integer

    def place(tag, room, qty, x):
        vs.Rect(x, 0, x + 1.0, 0.6)
        h = vs.LNewObj()
        vs.SetRecord(h, kRecName)
        vs.SetRField(h, kRecName, 'AssetTag',   tag)
        vs.SetRField(h, kRecName, 'RoomNumber', room)
        vs.SetRField(h, kRecName, 'Quantity',   str(qty))

    place('DESK-01',  '101', 1,  0.0)
    place('CHAIR-01', '101', 4,  2.0)
    place('LAMP-01',  '102', 2,  4.0)


def main():
    seed_test_objects()

    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)

    ws = vs.CreateWS(kWSName, 3, 3)

    # Row 1: static header text.
    cell(ws, 1, 1, 'Asset')
    cell(ws, 1, 2, 'Room')
    cell(ws, 1, 3, 'Qty')

    # Row 2: the database row. Column 0 receives the criteria; columns 1..N
    # receive the field references that appear in each subrow.
    vs.SetWSCellFormula(ws, 2, 0, 2, 0, db_criteria(kRecName))
    cell(ws, 2, 1, field_ref(kRecName, 'AssetTag'))
    cell(ws, 2, 2, field_ref(kRecName, 'RoomNumber'))
    cell(ws, 2, 3, field_ref(kRecName, 'Quantity'))

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message('Schedule populated from record "', kRecName, '"')


main()
```

## Anatomy of a Database Row
| Column | Content                              | Purpose                              |
|--------|--------------------------------------|--------------------------------------|
| 0      | `=DATABASE((R IN ['Furniture Info']))` | Selects which objects become subrows |
| 1      | `=('Furniture Info'.'AssetTag')`     | Pulls one field per subrow           |
| 2      | `=('Furniture Info'.'RoomNumber')`   | …                                    |

The database row itself acts as a **summary row** — it can hold aggregates
(count, sum) that fold the subrows below it (see example 26).

## Key Functions
- [`NewField`](../NewField.md), [`SetRecord`](../SetRecord.md), [`SetRField`](../SetRField.md)
- [`SetWSCellFormula`](../SetWSCellFormula.md), [`RecalculateWS`](../RecalculateWS.md), [`ShowWS`](../ShowWS.md)
