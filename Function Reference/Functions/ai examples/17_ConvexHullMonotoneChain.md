# 17. Convex Hull (Andrew's Monotone Chain)

## Description
Computes the convex hull of a scattered set of 2D points using Andrew's monotone
chain algorithm — a robust O(n log n) method that produces the vertices in
counter-clockwise order. Handy for tasks like "smallest enclosing shape",
finding the outer boundary of a survey point cloud, or computing site-envelope
polygons.

The script scatters a pseudo-random point cloud, drops a locus at every point,
computes the hull, and draws it as a highlighted polygon.

## What This Demonstrates
- Sorting points lexicographically and building lower + upper hulls
- Using the 2D cross product to decide left/right turns
- Deterministic pseudo-random point generation (no `random` import needed)

## Python Script
```python
import vs

# ---- 2D cross product (see 11_VectorMathToolkit.md for the full toolkit) ---
def _cross(o, a, b):
    return (a[0] - o[0]) * (b[1] - o[1]) - (a[1] - o[1]) * (b[0] - o[0])


def convex_hull(points):
    """Andrew's monotone chain. Returns hull vertices in CCW order.

    Removes duplicates first so degenerate inputs still yield a valid polygon.
    """
    pts = sorted(set((round(p[0], 9), round(p[1], 9)) for p in points))
    n = len(pts)
    if n < 3:
        return list(pts)

    # Build the lower hull.
    lower = []
    for p in pts:
        while len(lower) >= 2 and _cross(lower[-2], lower[-1], p) <= 0:
            lower.pop()
        lower.append(p)

    # Build the upper hull.
    upper = []
    for p in reversed(pts):
        while len(upper) >= 2 and _cross(upper[-2], upper[-1], p) <= 0:
            upper.pop()
        upper.append(p)

    # Concatenate; the last point of each half is the starting point of the
    # other half, so drop them to avoid duplicating the first/last vertex.
    return lower[:-1] + upper[:-1]


def scatter_pseudo_random(count, x_range=(0.0, 8.0), y_range=(0.0, 5.0),
                          seed=1_234_567_89):
    """Deterministic point cloud using a simple linear-congruential generator."""
    state = seed
    x0, x1 = x_range
    y0, y1 = y_range
    for _ in range(count):
        state = (state * 1_103_515_245 + 12345) & 0x7FFFFFFF
        u = state / 0x7FFFFFFF
        state = (state * 1_103_515_245 + 12345) & 0x7FFFFFFF
        v = state / 0x7FFFFFFF
        yield (x0 + u * (x1 - x0), y0 + v * (y1 - y0))


def draw_polygon(vertices):
    vs.BeginPoly()
    for x, y in vertices:
        vs.AddPoint(x, y)
    vs.AddPoint(vertices[0][0], vertices[0][1])
    vs.EndPoly()
    return vs.LNewObj()


def main():
    cloud = list(scatter_pseudo_random(count=80))

    for pt in cloud:
        vs.Locus(pt[0], pt[1])

    hull = convex_hull(cloud)
    draw_polygon(hull)

    vs.TextOrigin(0.0, -0.8)
    vs.CreateText(str(len(cloud)) + ' points -> hull of ' + str(len(hull)) + ' vertices')

main()
```

## Key VectorScript Functions Used
- [`BeginPoly`](../BeginPoly.md), [`AddPoint`](../AddPoint.md), [`EndPoly`](../EndPoly.md)
- [`Locus`](../Locus.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`LNewObj`](../LNewObj.md)
