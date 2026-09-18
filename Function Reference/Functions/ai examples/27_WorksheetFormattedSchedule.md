# 27. Formatted Wall Schedule

## Description
Extracts every wall on the active layer, reads its length, thickness and
overall height, and writes them into a *properly formatted* worksheet with
column widths, alignment, borders, a bold header row and number formatting
with a unit suffix. This is the level of polish the built-in wall/joist
schedules ship with in `Common/Includes/Property Line.px` and
`VW_Arch/Includes/Create Joists from Poly.px`.

## What This Demonstrates
- Reading wall geometry:
  [`GetSegPt1`](../GetSegPt1.md) /
  [`GetSegPt2`](../GetSegPt2.md),
  [`GetWallThickness`](../GetWallThickness.md),
  [`GetWallOverallHeights`](../GetWallOverallHeights.md),
  [`HLength`](../HLength.md)
- Full worksheet formatting:
  fonts, alignment, borders, column widths, row heights, number format

## Python Script
```python
import vs
import math

kWSName    = 'Wall Schedule'
_wallRows  = []


def _harvest_wall(h):
    p1 = vs.GetSegPt1(h)
    p2 = vs.GetSegPt2(h)
    length = math.hypot(p2[0] - p1[0], p2[1] - p1[1])
    ok, thk = vs.GetWallThickness(h)
    top, bot = vs.GetWallOverallHeights(h)
    _wallRows.append({
        'name':   vs.GetName(h) or '(unnamed)',
        'cls':    vs.GetClass(h) or '(none)',
        'length': length,
        'thk':    thk if ok else 0.0,
        'height': top - bot,
    })


def cell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def main():
    _wallRows.clear()
    layer_name = vs.GetLName(vs.ActLayer())
    vs.ForEachObject(_harvest_wall, "(T=WALL) & (L='" + layer_name + "')")

    if not _wallRows:
        vs.AlrtDialog('No walls on layer "' + layer_name + '".')
        return

    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)

    total_rows = len(_wallRows) + 2                     # header + rows + totals
    ws = vs.CreateWS(kWSName, total_rows, 5)

    headers = ('#', 'Name', 'Class', 'Length (m)', 'Thickness (mm)')
    for c, label in enumerate(headers, start=1):
        cell(ws, 1, c, label)

    # 1. Font + bold + centred for the header row.
    arial = vs.GetFontID('Arial')
    vs.SetWSCellTextFormat(ws, 1, 1, 1, 5, arial, 10, 1)   # 1 = bold
    vs.SetWSCellAlignment(ws, 1, 1, 1, 5, 2)               # centre

    # 2. Populate data rows.
    for i, r in enumerate(_wallRows, start=2):
        cell(ws, i, 1, str(i - 1))
        cell(ws, i, 2, r['name'])
        cell(ws, i, 3, r['cls'])
        cell(ws, i, 4, vs.Num2Str(3, r['length']))
        cell(ws, i, 5, vs.Num2Str(0, r['thk'] * 1000.0))   # m -> mm

    # 3. Totals row.
    total_row = total_rows
    cell(ws, total_row, 2, 'TOTAL')
    cell(ws, total_row, 4, '=SUM(D2:D' + str(len(_wallRows) + 1) + ')')
    vs.SetWSCellTextFormat(ws, total_row, 1, total_row, 5, arial, 10, 1)

    # 4. Number format: 2 decimals with " m" trailer on col 4, integer with
    #    " mm" trailer on col 5 (SetWSCellNumberFormat style 1 = general/text).
    vs.SetWSCellNumberFormat(ws, 2, 4, total_row, 4, 2, 2, '', ' m')
    vs.SetWSCellNumberFormat(ws, 2, 5, total_row, 5, 2, 0, '', ' mm')

    # 5. Column widths in pixels + first row taller.
    vs.SetWSColumnWidth(ws, 1, 1, 40)
    vs.SetWSColumnWidth(ws, 2, 3, 150)
    vs.SetWSColumnWidth(ws, 4, 5, 110)
    vs.SetWSRowHeight(ws, 1, 1, 22, True, True)

    # 6. Border: outline the whole table, thin lines between rows.
    vs.SetWSCellBorder(ws, 1, 1, total_rows, 5,
                       True, True, True, True, True)

    # 7. Right-align numeric columns.
    vs.SetWSCellAlignment(ws, 2, 4, total_row, 5, 4)       # 4 = right

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message(str(len(_wallRows)), ' walls tabulated with formatting.')


main()
```

## Formatting Cheat-Sheet
| Call                                                             | Purpose                              |
|------------------------------------------------------------------|--------------------------------------|
| `SetWSCellTextFormat(ws, r1, c1, r2, c2, fontID, size, style)`   | font, point-size, style bits (0/1/2/4) |
| `SetWSCellAlignment(ws, r1, c1, r2, c2, alignment)`              | 1 = general, 2 = centre, 3 = left, 4 = right |
| `SetWSColumnWidth(ws, from, to, pixels)`                         | column width in pixels               |
| `SetWSRowHeight(ws, from, to, pixels, updatePalette, lockHeight)`| row height in pixels                 |
| `SetWSCellBorder(ws, r1, c1, r2, c2, top, left, bot, right, outline)` | boolean per edge; outline = true → outer only |
| `SetWSCellNumberFormat(ws, r1, c1, r2, c2, style, accuracy, leader, trailer)` | numeric formatting + prefix/suffix |

## Key Functions
- [`GetSegPt1`](../GetSegPt1.md), [`GetSegPt2`](../GetSegPt2.md), [`GetWallThickness`](../GetWallThickness.md), [`GetWallOverallHeights`](../GetWallOverallHeights.md)
- [`SetWSCellTextFormat`](../SetWSCellTextFormat.md), [`SetWSCellAlignment`](../SetWSCellAlignment.md), [`SetWSCellNumberFormat`](../SetWSCellNumberFormat.md)
- [`SetWSCellBorder`](../SetWSCellBorder.md), [`SetWSColumnWidth`](../SetWSColumnWidth.md), [`SetWSRowHeight`](../SetWSRowHeight.md)
- [`GetFontID`](../GetFontID.md)
