# 23. Count Objects by Criteria (Formula-Driven)

## Description
Instead of iterating from Python, we let Vectorworks tally the drawing itself
by writing worksheet formulas that use `=COUNT((criteria))`. The script builds
a small dashboard: total selected count, rectangles, polylines, walls,
symbols by name, and one class-specific tally. This is the technique the
Spotlight cable/hoist worksheets use in `VW_Spotlight/Includes/CableTools`.

## What This Demonstrates
- Formula-driven object counting with `=COUNT((...))`
- Composing criteria strings inside cell formulas
- Using `vs.Count` from Python if you also want the number in code

## Python Script
```python
import vs

kWSName = 'Object Tally'


def cell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def count_formula(criteria):
    """Return a =COUNT worksheet formula for the given criteria string.

    Single quotes inside the criteria are doubled — that's how Pascal-style
    string literals escape a quote (' -> '').
    """
    return "=COUNT((" + criteria.replace("'", "''") + "))"


def main():
    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)

    ws = vs.CreateWS(kWSName, 10, 2)

    cell(ws, 1, 1, 'Metric')
    cell(ws, 1, 2, 'Count')

    # Broad tallies (VW does the work).
    cell(ws, 2, 1, 'Selected objects')
    cell(ws, 2, 2, count_formula('SEL=TRUE'))

    cell(ws, 3, 1, 'Rectangles')
    cell(ws, 3, 2, count_formula('T=RECT'))

    cell(ws, 4, 1, 'Polylines')
    cell(ws, 4, 2, count_formula('T=POLYLINE'))

    cell(ws, 5, 1, 'Walls')
    cell(ws, 5, 2, count_formula('T=WALL'))

    cell(ws, 6, 1, 'Symbols in class "Furniture"')
    cell(ws, 6, 2, count_formula("(T=SYMBOL) & (C='Furniture')"))

    cell(ws, 7, 1, 'Objects on active layer')
    active_layer_name = vs.GetLName(vs.ActLayer())
    cell(ws, 7, 2, count_formula("L='" + active_layer_name + "'"))

    # For contrast: same tally computed in Python and written as a value.
    py_count = vs.Count("SEL=TRUE")
    cell(ws, 9, 1, 'Selected (computed in Python)')
    cell(ws, 9, 2, vs.Num2Str(0, py_count))

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message('Tally worksheet created.')


main()
```

## When to Use Formula vs Iterate
- **Use `=COUNT` / `=SUM` / `=AREA` formulas** when the value must stay live
  as the user edits the drawing — the worksheet re-tallies on
  `RecalculateWS` and whenever VW is idle.
- **Iterate in Python** when you need conditional logic, derived properties
  or side-effects that formulas can't express.

## Key Functions
- [`SetWSCellFormula`](../SetWSCellFormula.md), [`Count`](../Count.md)
- [`ActLayer`](../ActLayer.md), [`GetLName`](../GetLName.md)
- [`Num2Str`](../Num2Str.md)
