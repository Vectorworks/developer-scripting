# 06. Boolean Solids: Drill a Hole Through a Block

## Description
Boolean operations are the workhorse of parametric mechanical parts. This
example builds a rectangular block, drills a cylindrical hole through it with
[`SubtractSolid`](../SubtractSolid.md), then unions a
smaller box on top with [`AddSolid`](../AddSolid.md). The
same pair of calls drives the cabinet and structural-shape plug-ins in
`Common/Includes`.

## What This Demonstrates
- Making a base solid with [`BeginXtrd`](../BeginXtrd.md) /
  [`EndXtrd`](../EndXtrd.md)
- Building a cutter, then subtracting it from a base with
  [`SubtractSolid`](../SubtractSolid.md)
- Unioning solids with [`AddSolid`](../AddSolid.md)
- Reading the result status returned by both functions

## Python Script
```python
import vs

# Result-code table (0 = success). See AddSolid.md for the full list.
kSolidOpSuccess = 0


def MakeBox(x1, y1, x2, y2, bottom, top):
    """Create a rectangular extrude and return its handle."""
    vs.BeginXtrd(bottom, top)
    vs.Rect(x1, y1, x2, y2)
    vs.EndXtrd()
    return vs.LNewObj()


def MakeCylinder(cx, cy, radius, bottom, top):
    """Create a cylindrical extrude and return its handle."""
    vs.BeginXtrd(bottom, top)
    vs.Oval(cx - radius, cy - radius, cx + radius, cy + radius)
    vs.EndXtrd()
    return vs.LNewObj()


def main():
    # --- Base block: 3 x 2 x 1 --------------------------------------------
    hBase = MakeBox(0.0, 0.0, 3.0, 2.0, bottom=0.0, top=1.0)

    # --- Cutter: cylinder centered on the block, taller so it pierces ----
    hHole = MakeCylinder(cx=1.5, cy=1.0, radius=0.35,
                         bottom=-0.1, top=1.1)

    # SubtractSolid(base, tool) -> (status, newSolidHandle).
    status, hDrilled = vs.SubtractSolid(hBase, hHole)
    if status != kSolidOpSuccess:
        vs.AlrtDialog('SubtractSolid failed with code ' + str(status))
        return

    # --- Second block: a small cap unioned onto the drilled block --------
    hCap = MakeBox(1.0, 0.5, 2.0, 1.5, bottom=1.0, top=1.4)

    status, hFinal = vs.AddSolid(hDrilled, hCap)
    if status != kSolidOpSuccess:
        vs.AlrtDialog('AddSolid failed with code ' + str(status))
        return

    vs.Message('Boolean part complete: base drilled and cap added.')

main()
```

## Key VectorScript Functions Used
- [`BeginXtrd`](../BeginXtrd.md), [`EndXtrd`](../EndXtrd.md)
- [`Rect`](../Rect.md), [`Oval`](../Oval.md)
- [`SubtractSolid`](../SubtractSolid.md), [`AddSolid`](../AddSolid.md)
- [`LNewObj`](../LNewObj.md)
- [`AlrtDialog`](../AlrtDialog.md), [`Message`](../Message.md)
