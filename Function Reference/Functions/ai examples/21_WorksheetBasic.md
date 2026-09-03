# 21. Hello Worksheet — Create and Populate

## Description
The smallest possible worksheet script: create a new worksheet, write a header
row and two literal data rows, tell Vectorworks to recalculate, and show it.
All later worksheet examples build on this pattern.

## What This Demonstrates
- Creating a worksheet with
  [`CreateWS`](../CreateWS.md)
- Writing text or formulas into a cell with
  [`SetWSCellFormula`](../SetWSCellFormula.md)
- Recalculating with
  [`RecalculateWS`](../RecalculateWS.md)
- Showing the worksheet window with
  [`ShowWS`](../ShowWS.md)

## Python Script
```python
import vs

kWSName = 'Hello WS'


def cell(ws, row, col, text):
    """Write literal text into a single cell.

    SetWSCellFormula uses a rectangular range; passing the same row/column
    for top-left and bottom-right addresses one cell.
    """
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def main():
    # Remove a stale worksheet with the same name so re-runs are idempotent.
    existing = vs.GetObject(kWSName)
    if existing is not None:
        vs.DelObject(existing)

    ws = vs.CreateWS(kWSName, 4, 3)         # 4 rows, 3 columns

    # Row 1: headers.
    cell(ws, 1, 1, 'Name')
    cell(ws, 1, 2, 'Class')
    cell(ws, 1, 3, 'Area')

    # Rows 2-3: literal example rows.
    cell(ws, 2, 1, 'Room-01')
    cell(ws, 2, 2, 'Spaces')
    cell(ws, 2, 3, '18.5')

    cell(ws, 3, 1, 'Room-02')
    cell(ws, 3, 2, 'Spaces')
    cell(ws, 3, 3, '22.0')

    # Row 4: a live formula. Anything starting with '=' is evaluated.
    cell(ws, 4, 3, '=B2+B3')                # will resolve to 40.5

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message('Created worksheet "', kWSName, '"')


main()
```

## Key Concepts
- **Row/column indices start at 1.** Row 0 (and column 0) are reserved for
  database rows — see example 24.
- **Everything is a formula string.** Numbers get stored as text unless the
  string starts with `=`. Use `vs.Num2Str(precision, value)` when writing a
  computed number.
- **Formula syntax mirrors spreadsheet conventions** (`=A1+B2`, `=SUM(A1:A3)`)
  plus VW-specific functions (`=COUNT((C='Walls-Exterior'))`, `=AREA`).

## Key Functions
- [`CreateWS`](../CreateWS.md)
- [`SetWSCellFormula`](../SetWSCellFormula.md)
- [`RecalculateWS`](../RecalculateWS.md)
- [`ShowWS`](../ShowWS.md), [`GetObject`](../GetObject.md), [`DelObject`](../DelObject.md)
