# 05. Turn a Column Profile with Sweep

## Description
`BeginSweep` / `EndSweep` produces a solid of revolution — a lathe operation.
The mechanical plug-ins (`Circular Stair`, `HVAC_Elbow`, screws, springs) all
use this pattern. Here we sweep a stepped polyline profile to make a classic
column shape and add a torus-shaped base plate around it.

## What This Demonstrates
- Building a solid of revolution with
  [`BeginSweep`](../BeginSweep.md) /
  [`EndSweep`](../EndSweep.md)
- Defining the swept profile with
  [`MoveTo`](../MoveTo.md) and
  [`LineTo`](../LineTo.md)
- Sweeping only part of the way around (partial revolution) to make a torus segment

## Python Script
```python
import vs


def SweepColumn(baseRadius, shaftRadius, topRadius, height, segments=32):
    r"""Sweep a stepped column profile 360 degrees about the origin.

    Profile drawn in the XZ plane (X is the radius, Y is elevation):

        top   ___
             |   \
             |    \    -> top of shaft
             |____|
             |    |    -> shaft
        base |____|_
                   \_  -> foot (chamfer)
    """
    # BeginSweep(startAngle, sweepAngle, incrementDegrees, riseFactor).
    vs.BeginSweep(0, 360, 360.0 / segments, 0)

    # Draw the profile counter-clockwise so the resulting normals face outward.
    baseHeight  = height * 0.10
    shaftHeight = height * 0.75
    footChamfer = baseRadius * 0.35

    vs.MoveTo(0.0,               0.0)
    vs.LineTo(baseRadius,        0.0)
    vs.LineTo(baseRadius,        baseHeight - footChamfer)
    vs.LineTo(baseRadius - footChamfer, baseHeight)
    vs.LineTo(shaftRadius,       baseHeight)
    vs.LineTo(shaftRadius,       baseHeight + shaftHeight)
    vs.LineTo(topRadius,         baseHeight + shaftHeight)
    vs.LineTo(topRadius,         height)
    vs.LineTo(0.0,               height)
    vs.LineTo(0.0,               0.0)

    vs.EndSweep()
    return vs.LNewObj()


def SweepTorusRing(innerRadius, tubeRadius, arcDegrees=360, segments=24):
    """Sweep a small circle (approximated as an octagon) to produce a ring."""
    vs.BeginSweep(0, arcDegrees, arcDegrees / segments, 0)

    # Octagonal profile approximating a circle of `tubeRadius` at X=innerRadius.
    import math
    sides = 8
    for i in range(sides + 1):
        angle = 2 * math.pi * i / sides
        px = innerRadius + tubeRadius * math.cos(angle)
        py = tubeRadius * math.sin(angle)
        if i == 0:
            vs.MoveTo(px, py)
        else:
            vs.LineTo(px, py)

    vs.EndSweep()
    return vs.LNewObj()


def main():
    hColumn = SweepColumn(baseRadius=0.30, shaftRadius=0.22,
                          topRadius=0.24,  height=3.0)

    # A full torus base ring around the column foot.
    hRing = SweepTorusRing(innerRadius=0.30, tubeRadius=0.04)

    vs.Message('Column and base ring swept.')

main()
```

## Key VectorScript Functions Used
- [`BeginSweep`](../BeginSweep.md), [`EndSweep`](../EndSweep.md)
- [`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md)
- [`LNewObj`](../LNewObj.md)
- [`Message`](../Message.md)
