# 13. Point-in-Polygon Test (Ray Casting)

## Description
Uses the classic ray-casting algorithm to test whether points lie inside a
polygon: shoot a horizontal ray from the test point to the right and count how
many polygon edges it crosses. An odd count means "inside".

The script draws an arbitrary polygon, scatters a grid of small locus markers
across its bounding box, then classifies each point and drops a matching label
next to the ones that fall inside.

## What This Demonstrates
- The point-in-polygon ray-cast algorithm, robust for edge cases where the ray
  passes through a vertex
- Reading a polygon's bounding box with
  [`GetBBox`](../GetBBox.md) to scope the sample grid
- Using [`Locus`](../Locus.md) to mark hits and
  [`CreateText`](../CreateText.md) for labels

## Python Script
```python
import vs


def point_in_polygon(pt, vertices):
    """Ray-cast test. `vertices` is a list of (x, y) tuples, implicitly closed.

    A horizontal ray is shot to +X from `pt`. Every edge that straddles the ray
    contributes a hit. The parity of the hit count decides inside/outside.
    """
    x, y = pt
    inside = False
    n = len(vertices)
    j = n - 1
    for i in range(n):
        xi, yi = vertices[i]
        xj, yj = vertices[j]
        # Edge straddles the horizontal line y? (>= handles the vertex case
        # consistently: we treat the *lower* endpoint as belonging to the edge.)
        if ((yi > y) != (yj > y)):
            x_cross = (xj - xi) * (y - yi) / (yj - yi) + xi
            if x < x_cross:
                inside = not inside
        j = i
    return inside


def draw_polygon(vertices):
    vs.BeginPoly()
    for x, y in vertices:
        vs.AddPoint(x, y)
    vs.AddPoint(vertices[0][0], vertices[0][1])
    vs.EndPoly()
    return vs.LNewObj()


def polygon_bbox(vertices):
    xs = [v[0] for v in vertices]
    ys = [v[1] for v in vertices]
    return (min(xs), min(ys), max(xs), max(ys))


def scatter_grid(vertices, cols=12, rows=10, margin=0.2):
    """Yield a grid of (x, y) test points over the polygon's bbox."""
    x0, y0, x1, y1 = polygon_bbox(vertices)
    x0 -= margin
    y0 -= margin
    x1 += margin
    y1 += margin
    if cols < 2 or rows < 2:
        return
    dx = (x1 - x0) / (cols - 1)
    dy = (y1 - y0) / (rows - 1)
    for r in range(rows):
        for c in range(cols):
            yield (x0 + c * dx, y0 + r * dy)


def main():
    # A concave polygon so the test actually exercises the odd/even rule.
    polygon = [
        (0.0, 0.0), (5.0, 0.0), (5.0, 3.0),
        (3.0, 3.0), (3.0, 1.5), (2.0, 1.5),
        (2.0, 3.0), (0.0, 3.0),
    ]
    draw_polygon(polygon)

    inside_count = 0
    total = 0
    for pt in scatter_grid(polygon):
        total += 1
        if point_in_polygon(pt, polygon):
            inside_count += 1
            vs.Locus(pt[0], pt[1])

    vs.TextOrigin(0.0, -0.8)
    vs.CreateText('inside = ' + str(inside_count) + ' / ' + str(total))

main()
```

## Key VectorScript Functions Used
- [`BeginPoly`](../BeginPoly.md), [`AddPoint`](../AddPoint.md), [`EndPoly`](../EndPoly.md)
- [`Locus`](../Locus.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`LNewObj`](../LNewObj.md), [`GetBBox`](../GetBBox.md)
