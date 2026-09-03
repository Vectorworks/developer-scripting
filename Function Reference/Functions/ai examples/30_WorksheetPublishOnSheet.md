# 30. Publish Worksheet Image on a Sheet Layer

## Description
End-to-end reporting pipeline:

1. Iterate the drawing to gather data.
2. Create + format a worksheet with the results.
3. Hide the worksheet window, promote it to a **worksheet image** placed on
   a Sheet Layer so it prints and exports.
4. Re-run the whole thing idempotently — deletes any prior image / sheet
   before rebuilding.

This is what production plug-ins do (see `Common/Includes/Property Line.px`,
`VW_Land/Includes/Choose Schedule.px` and `Create Drawing List.px`) to leave
a printable schedule attached to a title-block sheet.

## What This Demonstrates
- Programmatically creating a **sheet layer** and switching to it
- Placing a worksheet on the drawing with
  [`CreateWSImage`](../CreateWSImage.md)
- Hiding the worksheet window with
  [`ShowWS`](../ShowWS.md)`(ws, False)` — the image
  still updates
- Setting the placement/scale of the worksheet image object

## Python Script
```python
import vs

kSheetName = 'A-101 Schedule'
kWSName    = 'Object Report'
kImageObjName = 'Object Report WSImage'


# --------------------------------------------------------------------------
# 1. Data collection.
# --------------------------------------------------------------------------
_rows = []


def _row(h):
    _rows.append({
        'name': vs.GetName(h) or '(unnamed)',
        'cls':  vs.GetClass(h) or '(none)',
        'area': vs.HAreaN(h),
    })


# --------------------------------------------------------------------------
# 2. Idempotent cleanup helpers.
# --------------------------------------------------------------------------
def delete_if_exists(name):
    h = vs.GetObject(name)
    if h is not None:
        vs.DelObject(h)


# --------------------------------------------------------------------------
# 3. Worksheet build.
# --------------------------------------------------------------------------
def build_worksheet(rows):
    delete_if_exists(kWSName)
    ws = vs.CreateWS(kWSName, len(rows) + 2, 3)

    # Header.
    for c, label in enumerate(('Name', 'Class', 'Area'), start=1):
        vs.SetWSCellFormula(ws, 1, c, 1, c, label)
    vs.SetWSCellTextFormat(ws, 1, 1, 1, 3, vs.GetFontID('Arial'), 10, 1)

    # Data.
    for i, r in enumerate(rows, start=2):
        vs.SetWSCellFormula(ws, i, 1, i, 1, r['name'])
        vs.SetWSCellFormula(ws, i, 2, i, 2, r['cls'])
        vs.SetWSCellFormula(ws, i, 3, i, 3, vs.Num2Str(3, r['area']))

    # Totals.
    total_row = len(rows) + 2
    vs.SetWSCellFormula(ws, total_row, 1, total_row, 1, 'TOTAL')
    vs.SetWSCellFormula(ws, total_row, 3, total_row, 3,
                        '=SUM(C2:C' + str(len(rows) + 1) + ')')
    vs.SetWSCellTextFormat(ws, total_row, 1, total_row, 3,
                           vs.GetFontID('Arial'), 10, 1)

    # Presentation.
    vs.SetWSCellBorder(ws, 1, 1, total_row, 3, True, True, True, True, True)
    vs.SetWSColumnWidth(ws, 1, 2, 180)
    vs.SetWSColumnWidth(ws, 3, 3, 110)
    vs.SetWSCellAlignment(ws, 2, 3, total_row, 3, 4)     # right

    vs.RecalculateWS(ws)
    return ws


# --------------------------------------------------------------------------
# 4. Sheet + image placement.
# --------------------------------------------------------------------------
def publish_on_sheet(ws):
    # 4a. Create (or re-use) the sheet layer, make it active.
    delete_if_exists(kSheetName)                       # forces a fresh layer
    vs.CreateLayer(kSheetName, 2)                      # 2 = sheet layer
    vs.Layer(kSheetName)

    # 4b. Hide the on-screen worksheet window; the image still refreshes.
    vs.ShowWS(ws, False)

    # 4c. Drop a worksheet image at (0.2, 0.2) on the sheet.
    hImage = vs.CreateWSImage(ws, 0.2, 0.2)
    vs.SetName(hImage, kImageObjName)

    # 4d. Optional: scale the image so it prints at ~150 %.
    vs.SetWSImageScaleF(hImage, 1.5, True)
    return hImage


def main():
    _rows.clear()
    layer_name = vs.GetLName(vs.ActLayer())
    vs.ForEachObject(_row, "L='" + layer_name + "'")

    if not _rows:
        vs.AlrtDialog('Nothing on active layer to report.')
        return

    ws = build_worksheet(_rows)
    publish_on_sheet(ws)

    vs.Message('Published "', kWSName, '" on sheet "', kSheetName, '"')


main()
```

## Notes
- **Sheet Layers hold printable/annotation content**; they do not add to
  the model. Placing worksheet images (or viewport objects) is exactly
  what they exist for.
- **`ShowWS(ws, False)` doesn't disable updates.** The image still refreshes
  whenever the worksheet recalculates. The user can double-click the image
  to open the worksheet if they want to inspect the data.
- **Idempotency matters** — during script development the user will re-run
  the script many times. Deleting the previous sheet/image up-front avoids
  a growing pile of duplicate schedules.

## Progression Recap (Examples 21 → 30)
1. **21** — build the worksheet object
2. **22** — populate from an iterated selection
3. **23** — let VW count with `=COUNT`
4. **24** — self-populating database rows
5. **25** — geometric properties + `=SUM` grand totals
6. **26** — sort & group with `SetWSColumnOperators`
7. **27** — full visual formatting for a wall schedule
8. **28** — enumerate symbol definitions, live instance counts
9. **29** — aggregate across every design layer
10. **30** — publish the result on a sheet layer for output

## Key Functions
- [`CreateWS`](../CreateWS.md), [`SetWSCellFormula`](../SetWSCellFormula.md), [`RecalculateWS`](../RecalculateWS.md), [`ShowWS`](../ShowWS.md)
- [`CreateWSImage`](../CreateWSImage.md), [`SetWSImageScaleF`](../SetWSImageScaleF.md)
- [`CreateLayer`](../CreateLayer.md), [`Layer`](../Layer.md)
- [`SetName`](../SetName.md), [`GetObject`](../GetObject.md), [`DelObject`](../DelObject.md)
