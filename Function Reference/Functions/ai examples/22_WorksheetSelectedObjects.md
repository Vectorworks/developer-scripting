# 22. Selected Objects → Worksheet Rows

## Description
Iterates the current selection with `ForEachObject`, extracting the object's
name, class, layer, type code and 2D area, then writes one row per object into
a fresh worksheet. This is the manual reporting pattern used by the redline,
seating-layout and drawing-list plug-ins in `Common/Includes`.

## What This Demonstrates
- Collecting handles via
  [`ForEachObject`](../ForEachObject.md) with a criteria
  string (see also API doc §8)
- Two-pass structure: gather first, mutate/emit after (safe with the drawing
  list)
- Extracting object metadata with
  [`GetName`](../GetName.md),
  [`GetClass`](../GetClass.md),
  [`GetLayer`](../GetLayer.md),
  [`GetLName`](../GetLName.md),
  [`GetTypeN`](../GetTypeN.md),
  [`HAreaN`](../HAreaN.md)

## Python Script
```python
import vs

kWSName = 'Selected Objects'

# A minimal subset of type codes; see API doc §7.1 for the full table.
kTypeLabels = {
    2: 'Line', 3: 'Rect', 4: 'Oval', 5: 'Polygon', 6: 'Arc',
    10: 'Text', 11: 'Group', 15: 'Symbol', 17: '2D Locus', 21: 'Polyline',
    24: 'Extrude', 34: 'Sweep', 68: 'Wall', 71: 'Slab', 86: 'PIO',
}

_collected = []


def _collect(h):
    _collected.append(h)


def wcell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def main():
    _collected.clear()
    vs.ForEachObject(_collect, "SEL=TRUE")

    if not _collected:
        vs.AlrtDialog('Nothing is selected. Select some objects and re-run.')
        return

    # Fresh worksheet: one header row + one row per selected object.
    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)
    ws = vs.CreateWS(kWSName, len(_collected) + 1, 5)

    for col, label in enumerate(('Name', 'Class', 'Layer', 'Type', 'Area'), start=1):
        wcell(ws, 1, col, label)

    for i, h in enumerate(_collected, start=2):
        name  = vs.GetName(h) or '(unnamed)'
        cls   = vs.GetClass(h) or '(none)'
        layer = vs.GetLName(vs.GetLayer(h)) if vs.GetLayer(h) is not None else '(no layer)'
        tCode = vs.GetTypeN(h)
        tName = kTypeLabels.get(tCode, 'type ' + str(tCode))
        area  = vs.HAreaN(h)                # 0 for objects with no 2D area

        wcell(ws, i, 1, name)
        wcell(ws, i, 2, cls)
        wcell(ws, i, 3, layer)
        wcell(ws, i, 4, tName)
        wcell(ws, i, 5, vs.Num2Str(3, area))

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message(str(len(_collected)), ' selected object(s) reported.')


main()
```

## Notes
- **Numbers are written via `Num2Str`.** `HAreaN` returns a REAL — feed it
  to `Num2Str(precision, value)` before writing, otherwise the cell shows
  `0` instead of the number.
- **`ForEachObject` callback signature** is a single `HANDLE` and no return
  value. Share state via a module-level list (`_collected`).
- **`GetLayer(h)` can return `None`** for handles that aren't on a layer
  (e.g. items inside a symbol definition); guard before asking for its
  name.

## Key Functions
- [`ForEachObject`](../ForEachObject.md), [`CreateWS`](../CreateWS.md), [`SetWSCellFormula`](../SetWSCellFormula.md)
- [`GetName`](../GetName.md), [`GetClass`](../GetClass.md), [`GetLayer`](../GetLayer.md), [`GetLName`](../GetLName.md), [`GetTypeN`](../GetTypeN.md), [`HAreaN`](../HAreaN.md)
- [`Num2Str`](../Num2Str.md), [`RecalculateWS`](../RecalculateWS.md), [`ShowWS`](../ShowWS.md)
