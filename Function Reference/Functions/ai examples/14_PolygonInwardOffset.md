# 14. Polygon Inward / Outward Offset

## Description
Offsets every edge of a polygon by a signed distance and reconstructs the new
polygon by intersecting the offset lines pair-by-pair. Positive distances push
edges to the *left* of the traversal direction (inward for a CCW polygon);
negative distances push outward.

This is the classic building-footprint "shrink to inside wall" operation that
site-modifier and slab-edge tools rely on. Sharp inward corners can produce
self-intersections — the script deliberately keeps the offset small enough to
avoid that, so the algorithm stays readable.

## What This Demonstrates
- Building a signed edge offset with perpendicular vectors
- Intersecting two lines given a point and direction on each
- Handling convex and concave corners uniformly
- Drawing the original + offset polygons on the same layer for comparison

## Python Script
```python
import math
import vs

# ---- 2D vector helpers (see 11_VectorMathToolkit.md for the full toolkit) --
def v_sub(a, b): return (a[0] - b[0], a[1] - b[1])
def v_add(a, b): return (a[0] + b[0], a[1] + b[1])
def v_mul(a, s): return (a[0] * s, a[1] * s)
def v_len(a):    return math.hypot(a[0], a[1])
def v_norm(a):
    L = v_len(a)
    return (a[0] / L, a[1] / L) if L > 1e-12 else (0.0, 0.0)
# Left-perpendicular: rotate 90 CCW.
def v_perp(a):   return (-a[1], a[0])
def v_cross(a, b): return a[0] * b[1] - a[1] * b[0]


def line_line_intersect(p, r, q, s):
    """Intersect the line through `p` with direction `r` with the line through
    `q` with direction `s`. Returns `None` for parallel lines.
    """
    denom = v_cross(r, s)
    if abs(denom) < 1e-10:
        return None
    t = v_cross(v_sub(q, p), s) / denom
    return v_add(p, v_mul(r, t))


def offset_polygon(vertices, distance):
    """Offset a closed polygon by `distance` along each edge's left normal.

    For a CCW polygon a positive distance moves inward, a negative distance
    outward. The function returns a fresh list of (x, y) tuples.
    """
    n = len(vertices)
    if n < 3:
        return list(vertices)

    # 1. For each edge (i -> i+1) build an offset line: a point on it + direction.
    offset_lines = []
    for i in range(n):
        p = vertices[i]
        q = vertices[(i + 1) % n]
        edge_dir = v_sub(q, p)
        # Left-perpendicular normalised.
        normal = v_norm(v_perp(edge_dir))
        shift = v_mul(normal, distance)
        offset_lines.append((v_add(p, shift), edge_dir))

    # 2. Each new vertex is the intersection of the offset lines of the two
    #    edges that meet there. Parallel edges fall back to the raw offset.
    result = []
    for i in range(n):
        prev_line = offset_lines[(i - 1) % n]
        this_line = offset_lines[i]
        hit = line_line_intersect(prev_line[0], prev_line[1],
                                  this_line[0], this_line[1])
        if hit is None:
            hit = this_line[0]
        result.append(hit)
    return result


def draw_polygon(vertices):
    vs.BeginPoly()
    for x, y in vertices:
        vs.AddPoint(x, y)
    vs.AddPoint(vertices[0][0], vertices[0][1])
    vs.EndPoly()
    return vs.LNewObj()


def main():
    footprint = [
        (0.0, 0.0), (6.0, 0.0), (6.0, 3.0),
        (4.0, 3.0), (4.0, 4.5), (0.0, 4.5),
    ]
    draw_polygon(footprint)

    # Inward offset by 0.3 units (interior walls).
    inner = offset_polygon(footprint, 0.3)
    draw_polygon(inner)

    # Outward offset by 0.5 units (site setback).
    outer = offset_polygon(footprint, -0.5)
    draw_polygon(outer)

    vs.Message('Original + inward + outward offsets drawn.')

main()
```

## Key VectorScript Functions Used
- [`BeginPoly`](../BeginPoly.md), [`AddPoint`](../AddPoint.md), [`EndPoly`](../EndPoly.md)
- [`LNewObj`](../LNewObj.md)
- [`Message`](../Message.md)
- Compare with the built-in [`OffsetPoly`](../OffsetPoly.md) function
