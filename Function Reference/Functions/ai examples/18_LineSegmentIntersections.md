# 18. Line-Segment Intersection Finder

## Description
Given a bag of 2D line segments, finds every pair that crosses and drops a
locus at each intersection. The core primitive is a parametric line-line
solver — the same one used by the offset example (14) — extended with a
segment-range check so it only counts real crossings, not extensions of the
lines.

## What This Demonstrates
- A robust segment-segment intersection test using the 2D cross product
- Iterating over all unordered pairs of segments
- Distinguishing "cross", "endpoint touch" and "parallel/coincident"
- Marking each intersection with a small locus + label

## Python Script
```python
import vs

# -------------------------------------------------------------------------
# Return the intersection point of segments (p, p+r) and (q, q+s), or None.
# Uses the standard t/u parametric form (see Antonio's algorithm).
# -------------------------------------------------------------------------
def segment_intersect(p, r, q, s, eps=1e-9):
    rxs = r[0] * s[1] - r[1] * s[0]
    qp  = (q[0] - p[0], q[1] - p[1])
    qpxr = qp[0] * r[1] - qp[1] * r[0]

    if abs(rxs) < eps:
        # Parallel (rxs == 0). Collinear if qpxr == 0; treat as no crossing.
        return None

    t = (qp[0] * s[1] - qp[1] * s[0]) / rxs
    u = (qp[0] * r[1] - qp[1] * r[0]) / rxs

    if -eps <= t <= 1 + eps and -eps <= u <= 1 + eps:
        return (p[0] + t * r[0], p[1] + t * r[1])
    return None


def find_all_intersections(segments):
    """Return a list of (point, i, j) for every pair (i < j) that crosses."""
    hits = []
    n = len(segments)
    for i in range(n):
        (a, b) = segments[i]
        r = (b[0] - a[0], b[1] - a[1])
        for j in range(i + 1, n):
            (c, d) = segments[j]
            s = (d[0] - c[0], d[1] - c[1])
            pt = segment_intersect(a, r, c, s)
            if pt is None:
                continue
            # Skip trivial endpoint coincidences (shared vertex, not a cross).
            same_endpoint = (pt[0] - a[0]) ** 2 + (pt[1] - a[1]) ** 2 < 1e-14 \
                         or (pt[0] - b[0]) ** 2 + (pt[1] - b[1]) ** 2 < 1e-14 \
                         or (pt[0] - c[0]) ** 2 + (pt[1] - c[1]) ** 2 < 1e-14 \
                         or (pt[0] - d[0]) ** 2 + (pt[1] - d[1]) ** 2 < 1e-14
            if same_endpoint:
                continue
            hits.append((pt, i, j))
    return hits


def draw_segment(a, b):
    vs.MoveTo(a[0], a[1])
    vs.LineTo(b[0], b[1])


def main():
    # A grid of lines that intentionally crosses at many interior points.
    segments = [
        ((0.0, 0.0), (5.0, 3.0)),
        ((0.0, 3.0), (5.0, 0.0)),
        ((0.5, 1.5), (4.5, 1.5)),
        ((2.5, -0.5), (2.5, 3.5)),
        ((1.0, 0.5), (4.0, 2.8)),
        ((1.0, 2.8), (4.0, 0.5)),
    ]

    for a, b in segments:
        draw_segment(a, b)

    hits = find_all_intersections(segments)
    for k, (pt, _i, _j) in enumerate(hits, start=1):
        vs.Locus(pt[0], pt[1])
        vs.TextOrigin(pt[0] + 0.05, pt[1] + 0.05)
        vs.CreateText(str(k))

    vs.Message(str(len(hits)) + ' crossings found among '
               + str(len(segments)) + ' segments.')

main()
```

## Key VectorScript Functions Used
- [`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md)
- [`Locus`](../Locus.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`Message`](../Message.md)
- Related: [`LineLineIntersection`](../LineLineIntersection.md) if you prefer a built-in solver
