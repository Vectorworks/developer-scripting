# 12. Polygon Area and Centroid (Shoelace Formula)

## Description
Given the vertices of a closed polygon, computes the signed area and centroid
using the shoelace / surveyor formula. The signed area also tells you whether
the vertex order is clockwise (negative) or counter-clockwise (positive), which
matters for offsetting and boolean operations.

The script draws two polygons — a simple L-shape and a triangle — then places a
locus at each centroid and prints the area next to it.

## What This Demonstrates
- The shoelace formula for polygon signed area
- Centroid computation for a general non-self-intersecting polygon
- Detecting vertex-order (CW / CCW) from the sign of the area
- Placing loci and text labels with
  [`Locus`](../Locus.md) and
  [`CreateText`](../CreateText.md)

## Python Script
```python
import vs

# -------------------------------------------------------------------------
# Signed area (positive = CCW).  vertices is a list of (x, y) tuples.
# The polygon is assumed closed implicitly (first vertex is *not* repeated).
# -------------------------------------------------------------------------
def polygon_signed_area(vertices):
    n = len(vertices)
    if n < 3:
        return 0.0
    total = 0.0
    for i in range(n):
        x1, y1 = vertices[i]
        x2, y2 = vertices[(i + 1) % n]
        total += x1 * y2 - x2 * y1
    return total * 0.5


def polygon_area(vertices):
    return abs(polygon_signed_area(vertices))


def polygon_centroid(vertices):
    """Return the (Cx, Cy) centroid of a non-self-intersecting polygon.

    Uses the standard weighted-triangle-fan formula. Falls back to the
    vertex average if the polygon is degenerate (zero area).
    """
    n = len(vertices)
    signed_a = polygon_signed_area(vertices)
    if abs(signed_a) < 1e-12:
        sx = sum(v[0] for v in vertices) / n
        sy = sum(v[1] for v in vertices) / n
        return (sx, sy)

    cx = 0.0
    cy = 0.0
    for i in range(n):
        x1, y1 = vertices[i]
        x2, y2 = vertices[(i + 1) % n]
        cross = x1 * y2 - x2 * y1
        cx += (x1 + x2) * cross
        cy += (y1 + y2) * cross
    factor = 1.0 / (6.0 * signed_a)
    return (cx * factor, cy * factor)


def draw_polygon(vertices):
    """Emit the vertices as a Vectorworks polygon and return the handle."""
    vs.BeginPoly()
    for x, y in vertices:
        vs.AddPoint(x, y)
    # Close explicitly by repeating the first vertex.
    vs.AddPoint(vertices[0][0], vertices[0][1])
    vs.EndPoly()
    return vs.LNewObj()


def report_polygon(name, vertices):
    """Draw the polygon, place a locus at the centroid, print stats."""
    draw_polygon(vertices)
    area = polygon_area(vertices)
    cx, cy = polygon_centroid(vertices)
    orientation = 'CCW' if polygon_signed_area(vertices) > 0 else 'CW'

    vs.Locus(cx, cy)
    vs.TextOrigin(cx + 0.1, cy + 0.1)
    vs.CreateText(name + ': A=' + vs.Num2Str(3, area) + ' (' + orientation + ')')


def main():
    # 1. L-shaped polygon, CCW.
    l_shape = [
        (0.0, 0.0), (3.0, 0.0), (3.0, 1.5),
        (1.5, 1.5), (1.5, 3.0), (0.0, 3.0),
    ]
    report_polygon('L-shape', l_shape)

    # 2. Triangle shifted to the right, deliberately CW to show the sign.
    triangle_cw = [(6.0, 0.0), (6.0, 2.0), (8.0, 0.0)]
    report_polygon('Triangle', triangle_cw)

main()
```

## Key VectorScript Functions Used
- [`BeginPoly`](../BeginPoly.md), [`AddPoint`](../AddPoint.md), [`EndPoly`](../EndPoly.md)
- [`Locus`](../Locus.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`Num2Str`](../Num2Str.md)
- [`LNewObj`](../LNewObj.md)
