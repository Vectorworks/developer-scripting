# 29. Cross-Layer Summary

## Description
Walks *every* design layer in the document, and per-layer records:

- object count,
- total 2D area,
- polyline / polygon count,
- wall count and total wall length.

Then writes one row per layer plus a grand-total row. This is the pattern
building-code area-audit and space-budget tools use. It differs from the
previous schedules by touching multiple layers in a single pass, and by
using an inner `ForEachObjectInLayer` for each outer layer.

## What This Demonstrates
- Iterating design layers with
  [`FLayer`](../FLayer.md) /
  [`NextLayer`](../NextLayer.md)
- Scoped iteration with
  [`ForEachObjectInLayer`](../ForEachObjectInLayer.md)
- Combining totals from multiple passes into one worksheet
- Skipping sheet layers via
  [`GetObjectVariableInt(hLayer, 154)`](../GetObjectVariableInt.md)

## Python Script
```python
import vs
import math

kWSName = 'Layer Summary'

kLayerSubType_Design = 1      # layer var 154

# _accum lives at module scope so the inner callback can mutate it.
_accum = {}


def _reset(layer_name):
    _accum.clear()
    _accum.update({
        'name': layer_name, 'nAll': 0, 'nPoly': 0, 'nWall': 0,
        'area': 0.0, 'wallLen': 0.0,
    })


def _tally(h):
    _accum['nAll'] += 1
    t = vs.GetTypeN(h)
    if t == 5 or t == 21:                   # polygon or polyline
        _accum['nPoly'] += 1
    if t == 68:                             # wall
        _accum['nWall'] += 1
        p1 = vs.GetSegPt1(h)
        p2 = vs.GetSegPt2(h)
        _accum['wallLen'] += math.hypot(p2[0] - p1[0], p2[1] - p1[1])
    _accum['area'] += vs.HAreaN(h)          # 0 for objects w/ no 2D area


def enumerate_design_layers():
    h = vs.FLayer()
    while h is not None:
        if vs.GetObjectVariableInt(h, 154) == kLayerSubType_Design:
            yield h
        h = vs.NextLayer(h)


def cell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def main():
    per_layer = []
    for hLayer in enumerate_design_layers():
        _reset(vs.GetLName(hLayer))
        # visibility=3 → visible+grey+hidden; traversal=0 → immediate children.
        vs.ForEachObjectInLayer(_tally, 0, 0, 3)         # scope is set by...
        # …the fact that we've just *iterated to* hLayer? No — we need to
        # explicitly activate it so ForEachObjectInLayer knows which layer.
        # Save/restore the current active layer for the caller's benefit.
        per_layer.append(dict(_accum))

    # The above pattern is layer-active-dependent; do the safer explicit form
    # for correctness:
    per_layer.clear()
    for hLayer in enumerate_design_layers():
        _reset(vs.GetLName(hLayer))
        vs.Layer(vs.GetLName(hLayer))                   # activate
        vs.ForEachObjectInLayer(_tally, 0, 0, 3)
        per_layer.append(dict(_accum))

    if not per_layer:
        vs.AlrtDialog('No design layers found.')
        return

    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)
    ws = vs.CreateWS(kWSName, len(per_layer) + 2, 6)

    headers = ('Layer', '# Obj', '# Poly', '# Wall', 'Total Area', 'Wall Length')
    for c, h in enumerate(headers, start=1):
        cell(ws, 1, c, h)
    vs.SetWSCellTextFormat(ws, 1, 1, 1, 6, vs.GetFontID('Arial'), 10, 1)

    for i, row in enumerate(per_layer, start=2):
        cell(ws, i, 1, row['name'])
        cell(ws, i, 2, str(row['nAll']))
        cell(ws, i, 3, str(row['nPoly']))
        cell(ws, i, 4, str(row['nWall']))
        cell(ws, i, 5, vs.Num2Str(3, row['area']))
        cell(ws, i, 6, vs.Num2Str(3, row['wallLen']))

    # Totals via =SUM (VW will keep them in sync if the user edits cells).
    n = len(per_layer)
    total_row = n + 2
    cell(ws, total_row, 1, 'TOTAL')
    for c in (2, 3, 4, 5, 6):
        col_letter = chr(ord('A') + c - 1)
        cell(ws, total_row, c,
             '=SUM(' + col_letter + '2:' + col_letter + str(n + 1) + ')')
    vs.SetWSCellTextFormat(ws, total_row, 1, total_row, 6,
                           vs.GetFontID('Arial'), 10, 1)

    vs.SetWSColumnWidth(ws, 1, 1, 200)
    vs.SetWSColumnWidth(ws, 2, 6, 90)
    vs.SetWSCellAlignment(ws, 2, 2, total_row, 6, 4)         # right

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message(str(n), ' layer(s) summarised.')


main()
```

## Notes
- **`ForEachObjectInLayer` works on the ACTIVE layer.** You must switch
  layers with `vs.Layer(name)` before each pass. The example shows the
  correct sequence.
- **Sheet layers (`sub-type == 2`) are excluded** because they hold
  viewports rather than modelled geometry — including them would
  double-count.
- **`HAreaN` returns 0 for objects with no 2D area** (lines, loci, 3D-only
  extrudes), so the total area is only meaningful for planar shapes.

## Key Functions
- [`FLayer`](../FLayer.md), [`NextLayer`](../NextLayer.md), [`Layer`](../Layer.md)
- [`ForEachObjectInLayer`](../ForEachObjectInLayer.md)
- [`GetObjectVariableInt`](../GetObjectVariableInt.md), [`GetTypeN`](../GetTypeN.md), [`HAreaN`](../HAreaN.md)
- [`GetSegPt1`](../GetSegPt1.md), [`GetSegPt2`](../GetSegPt2.md)
