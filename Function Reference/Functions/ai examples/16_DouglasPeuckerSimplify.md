# 16. Polyline Simplification (Douglas-Peucker)

## Description
Reduces the number of vertices in a polyline while preserving its overall shape
by using the classic Ramer-Douglas-Peucker algorithm. This is what CAD packages
call "reduce points" or "simplify"; it's essential when you import survey data
or GIS contours and want to slim them down before further processing.

The script generates a wiggly polyline with 200 vertices, then draws it twice —
once original, once simplified with a tolerance — so the vertex reduction is
visible at a glance.

## What This Demonstrates
- The recursive Douglas-Peucker simplification algorithm
- Computing the perpendicular distance from a point to a line segment
- How increasing the tolerance trades off fidelity for vertex count

## Python Script
```python
import math
import vs


def _perp_distance(pt, a, b):
    """Perpendicular distance from `pt` to the segment `a`->`b`.

    Falls back to the endpoint distance when the segment is degenerate.
    """
    ax, ay = a
    bx, by = b
    dx, dy = bx - ax, by - ay
    seg_len_sq = dx * dx + dy * dy
    if seg_len_sq < 1e-18:
        return math.hypot(pt[0] - ax, pt[1] - ay)
    # Cross-product magnitude of (b-a) x (pt-a) divided by |b-a|.
    return abs(dx * (ay - pt[1]) - (ax - pt[0]) * dy) / math.sqrt(seg_len_sq)


def _simplify_range(points, first, last, tolerance, keep):
    """Recursive Douglas-Peucker over points[first..last] (inclusive)."""
    max_dist = 0.0
    max_idx = -1
    a = points[first]
    b = points[last]
    for i in range(first + 1, last):
        d = _perp_distance(points[i], a, b)
        if d > max_dist:
            max_dist = d
            max_idx = i
    if max_dist > tolerance and max_idx != -1:
        _simplify_range(points, first, max_idx, tolerance, keep)
        _simplify_range(points, max_idx, last, tolerance, keep)
    else:
        keep.add(last)


def simplify_polyline(points, tolerance):
    """Return a reduced list of vertices that stay within `tolerance` of the original."""
    n = len(points)
    if n < 3:
        return list(points)
    keep = {0}
    _simplify_range(points, 0, n - 1, tolerance, keep)
    return [points[i] for i in sorted(keep)]


def draw_polyline(vertices, yShift=0.0):
    for i in range(len(vertices) - 1):
        x1, y1 = vertices[i]
        x2, y2 = vertices[i + 1]
        vs.MoveTo(x1, y1 + yShift)
        vs.LineTo(x2, y2 + yShift)


def make_wiggly_path(count=200):
    """Generate a compound sine wave sampled at `count` points."""
    path = []
    for i in range(count):
        t = i / (count - 1)
        x = 12.0 * t
        y = math.sin(t * 6.0) + 0.4 * math.sin(t * 25.0)
        path.append((x, y))
    return path


def main():
    original = make_wiggly_path(count=200)
    draw_polyline(original, yShift=0.0)
    for pt in original:
        vs.Locus(pt[0], pt[1])

    for i, tol in enumerate((0.05, 0.15, 0.30), start=1):
        reduced = simplify_polyline(original, tol)
        draw_polyline(reduced, yShift=-2.5 * i)
        for pt in reduced:
            vs.Locus(pt[0], pt[1] - 2.5 * i)
        vs.TextOrigin(-0.6, -2.5 * i)
        vs.CreateText('tol=' + vs.Num2Str(2, tol)
                      + '  ' + str(len(reduced)) + ' pts')

    vs.Message('Original 200 pts vs. simplified at 3 tolerances.')

main()
```

## Key VectorScript Functions Used
- [`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md)
- [`Locus`](../Locus.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`Num2Str`](../Num2Str.md), [`Message`](../Message.md)
