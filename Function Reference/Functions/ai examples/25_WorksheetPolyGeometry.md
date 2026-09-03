# 25. Geometric Property Extraction Table

## Description
Iterates every polygon and polyline on the active layer, computes several
geometric properties (area, perimeter, vertex count, closed-ness, centroid),
and writes them into a formatted table. Real-world use: quantity take-off,
site-plan tallies, or a QA report before an export.

## What This Demonstrates
- Filtering the iterator by object type at the criteria level (fast)
- Reading geometric primitives:
  [`HAreaN`](../HAreaN.md),
  [`HPerimN`](../HPerimN.md),
  [`GetVertNum`](../GetVertNum.md),
  [`IsPolyClosed`](../IsPolyClosed.md),
  [`Centroid`](../Centroid.md)
- Grand-total footer row using `=SUM(...)` on the collected numbers

## Python Script
```python
import vs

kWSName = 'Poly Geometry'
_rows = []          # list of dict rows populated by the callback


def _harvest(h):
    ok, cx, cy = vs.Centroid(h)
    _rows.append({
        'name':    vs.GetName(h) or '(unnamed)',
        'type':    'Polyline' if vs.GetTypeN(h) == 21 else 'Polygon',
        'area':    vs.HAreaN(h),
        'perim':   vs.HPerimN(h),
        'nverts':  vs.GetVertNum(h),
        'closed':  vs.IsPolyClosed(h),
        'cx':      cx if ok else 0.0,
        'cy':      cy if ok else 0.0,
    })


def cell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def main():
    _rows.clear()
    layer_name = vs.GetLName(vs.ActLayer())
    criteria = "((T=POLY) | (T=POLYLINE)) & (L='" + layer_name + "')"
    vs.ForEachObject(_harvest, criteria)

    if not _rows:
        vs.AlrtDialog('No polygons or polylines on this layer.')
        return

    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)

    # header + N data rows + 1 totals row.
    ws = vs.CreateWS(kWSName, len(_rows) + 2, 7)

    for col, label in enumerate(
            ('Name', 'Type', 'Verts', 'Closed', 'Area', 'Perimeter', 'Centroid'),
            start=1):
        cell(ws, 1, col, label)

    for i, r in enumerate(_rows, start=2):
        cell(ws, i, 1, r['name'])
        cell(ws, i, 2, r['type'])
        cell(ws, i, 3, str(r['nverts']))
        cell(ws, i, 4, 'yes' if r['closed'] else 'no')
        cell(ws, i, 5, vs.Num2Str(3, r['area']))
        cell(ws, i, 6, vs.Num2Str(3, r['perim']))
        cell(ws, i, 7, '(' + vs.Num2Str(2, r['cx']) + ', '
                          + vs.Num2Str(2, r['cy']) + ')')

    # Totals row driven by =SUM over the range we just filled.
    total_row = len(_rows) + 2
    cell(ws, total_row, 1, 'TOTAL')
    cell(ws, total_row, 5, '=SUM(E2:E' + str(len(_rows) + 1) + ')')
    cell(ws, total_row, 6, '=SUM(F2:F' + str(len(_rows) + 1) + ')')

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message(str(len(_rows)), ' polys reported on layer "', layer_name, '"')


main()
```

## Notes
- **`HAreaN` returns 0 for open polylines.** If you need the outline length
  for open shapes, use `HPerimN` (perimeter degenerates to arc-length there).
- **The `=SUM(E2:E10)` formula uses spreadsheet A1 notation** even though
  cells are addressed as `(row, col)` from Python. Cheat sheet: column 1 →
  `A`, column 2 → `B`, … column 26 → `Z`.
- Combine this pattern with the sort/group operators from example 26 for
  a fully summarised report.

## Key Functions
- [`ForEachObject`](../ForEachObject.md), [`HAreaN`](../HAreaN.md), [`HPerimN`](../HPerimN.md), [`GetVertNum`](../GetVertNum.md), [`IsPolyClosed`](../IsPolyClosed.md), [`Centroid`](../Centroid.md)
- [`SetWSCellFormula`](../SetWSCellFormula.md), [`Num2Str`](../Num2Str.md)
