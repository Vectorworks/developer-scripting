# 04. Extrude 2D Shapes into 3D Solids

## Description
Uses the `BeginXtrd` / `EndXtrd` pair — the same one the cabinet and structural
shape plug-ins use — to promote a 2D profile into a 3D extrude. This example
extrudes a rectangle, an oval and a custom polygon at different heights, then
moves the resulting solids so they line up next to each other.

## What This Demonstrates
- Wrapping any 2D drawing block in
  [`BeginXtrd`](../BeginXtrd.md) /
  [`EndXtrd`](../EndXtrd.md) to build an extrude
- Placing the extrude at an arbitrary base/top elevation
- Getting the resulting 3D solid handle with
  [`LNewObj`](../LNewObj.md) and repositioning it with
  [`Move3DObj`](../Move3DObj.md)

## Python Script
```python
import vs


def ExtrudeRect(x1, y1, x2, y2, bottom, top):
    """Extrude a rectangle between the given elevations."""
    vs.BeginXtrd(bottom, top)
    vs.Rect(x1, y1, x2, y2)
    vs.EndXtrd()
    return vs.LNewObj()


def ExtrudeOval(cx, cy, radiusX, radiusY, bottom, top):
    """Extrude an oval defined by its center and two radii."""
    vs.BeginXtrd(bottom, top)
    vs.Oval(cx - radiusX, cy - radiusY, cx + radiusX, cy + radiusY)
    vs.EndXtrd()
    return vs.LNewObj()


def ExtrudePolygon(points, bottom, top):
    """Extrude a closed polygon defined by an iterable of (x, y) tuples."""
    vs.BeginXtrd(bottom, top)
    vs.BeginPoly()
    for x, y in points:
        vs.AddPoint(x, y)
    # Repeat the first vertex to close the polygon.
    vs.AddPoint(points[0][0], points[0][1])
    vs.EndPoly()
    vs.EndXtrd()
    return vs.LNewObj()


def main():
    # A 2 x 1 x 2.5 box positioned at the origin.
    hBox = ExtrudeRect(0.0, 0.0, 2.0, 1.0, bottom=0.0, top=2.5)

    # A cylinder (extruded oval) with equal radii of 0.6.
    hCylinder = ExtrudeOval(cx=4.0, cy=0.5, radiusX=0.6, radiusY=0.6,
                            bottom=0.0, top=2.0)

    # A triangular prism using a custom polygon.
    triangle = [(6.0, 0.0), (7.5, 0.0), (6.75, 1.3)]
    hPrism = ExtrudePolygon(triangle, bottom=0.0, top=1.5)

    # Slide the cylinder up 3m in Z to compare heights.
    vs.Move3DObj(hCylinder, 0.0, 0.0, 3.0)

    vs.Message('Three 3D extrudes created.')

main()
```

## Key VectorScript Functions Used
- [`BeginXtrd`](../BeginXtrd.md), [`EndXtrd`](../EndXtrd.md)
- [`Rect`](../Rect.md), [`Oval`](../Oval.md)
- [`BeginPoly`](../BeginPoly.md), [`AddPoint`](../AddPoint.md), [`EndPoly`](../EndPoly.md)
- [`LNewObj`](../LNewObj.md)
- [`Move3DObj`](../Move3DObj.md)
- [`Message`](../Message.md)
