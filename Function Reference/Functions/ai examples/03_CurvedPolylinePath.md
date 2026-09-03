# 03. Build a Curved Path with Mixed Vertex Types

## Description
Constructs a polyline that mixes corner, radius, and arc vertices — the same
technique the roadway and site-modifier plug-ins use to model curbs and
alignments. The script draws two paths side-by-side so you can compare a
straight polyline against one with rounded corners.

## What This Demonstrates
- Building polylines with [`BeginPoly`](../BeginPoly.md) /
  [`EndPoly`](../EndPoly.md)
- Adding vertices of different kinds with
  [`Add2DVertex`](../Add2DVertex.md)
  (0 = corner, 1 = bezier, 2 = cubic, 3 = arc, 4 = radius)
- Grabbing the resulting object handle with
  [`LNewObj`](../LNewObj.md) and turning it into a filled
  polyline through [`SetObjectVariableBoolean`](../SetObjectVariableBoolean.md)

## Python Script
```python
import vs

# Vertex type constants (see Add2DVertex remarks).
kCorner, kBezier, kCubic, kArc, kRadius = 0, 1, 2, 3, 4

# Selector 800 = "Object closed" for polylines. See Appendix E in the docs.
kSelector_IsClosed = 800


def DrawStraightPath(offsetY):
    """Draw a polyline with sharp corners along the given Y offset."""
    vs.BeginPoly()
    vs.Add2DVertex(0.0,  offsetY,        kCorner, 0)
    vs.Add2DVertex(2.0,  offsetY,        kCorner, 0)
    vs.Add2DVertex(2.0,  offsetY + 1.5,  kCorner, 0)
    vs.Add2DVertex(5.0,  offsetY + 1.5,  kCorner, 0)
    vs.Add2DVertex(5.0,  offsetY,        kCorner, 0)
    vs.Add2DVertex(7.0,  offsetY,        kCorner, 0)
    vs.EndPoly()
    return vs.LNewObj()


def DrawRoundedPath(offsetY, filletRadius):
    """Same footprint as DrawStraightPath but with rounded corners."""
    vs.BeginPoly()
    vs.Add2DVertex(0.0,  offsetY,        kCorner, 0)
    vs.Add2DVertex(2.0,  offsetY,        kRadius, filletRadius)
    vs.Add2DVertex(2.0,  offsetY + 1.5,  kRadius, filletRadius)
    vs.Add2DVertex(5.0,  offsetY + 1.5,  kRadius, filletRadius)
    vs.Add2DVertex(5.0,  offsetY,        kRadius, filletRadius)
    vs.Add2DVertex(7.0,  offsetY,        kCorner, 0)
    vs.EndPoly()
    return vs.LNewObj()


def DrawClosedArcLoop(centerX, centerY, radius):
    """Close a poly with type-3 arc vertices to draw a rounded pill."""
    vs.BeginPoly()
    vs.Add2DVertex(centerX - radius, centerY,          kArc, radius)
    vs.Add2DVertex(centerX,          centerY + radius, kArc, radius)
    vs.Add2DVertex(centerX + radius, centerY,          kArc, radius)
    vs.Add2DVertex(centerX,          centerY - radius, kArc, radius)
    vs.EndPoly()
    hLoop = vs.LNewObj()
    # Mark the polyline as closed so it fills correctly.
    vs.SetObjectVariableBoolean(hLoop, kSelector_IsClosed, True)
    return hLoop


def main():
    hStraight = DrawStraightPath(offsetY=0.0)
    hRounded  = DrawRoundedPath(offsetY=-3.0, filletRadius=0.4)
    hLoop     = DrawClosedArcLoop(centerX=9.0, centerY=-1.5, radius=1.2)

    vs.Message('Straight, rounded and closed-arc polylines drawn.')

main()
```

## Key VectorScript Functions Used
- [`BeginPoly`](../BeginPoly.md), [`EndPoly`](../EndPoly.md)
- [`Add2DVertex`](../Add2DVertex.md)
- [`LNewObj`](../LNewObj.md)
- [`SetObjectVariableBoolean`](../SetObjectVariableBoolean.md)
- [`Message`](../Message.md)
