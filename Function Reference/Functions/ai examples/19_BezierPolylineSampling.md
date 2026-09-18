# 19. Cubic Bezier Sampled to a Polyline

## Description
Approximates one or more cubic Bezier curves as a polyline by sampling them at
regular parameter intervals, then feeds the samples straight into
`vs.BeginPoly` / `vs.Add2DVertex`. The script also draws the control polygon
faintly so you can see the classic Bezier hull-in / curve-out relationship.

This is the same fundamental sampling step that vector graphics importers use
when they lower SVG / PostScript paths into Vectorworks polylines.

## What This Demonstrates
- The cubic Bezier basis expressed compactly with `binomial * (1-t)^k * t^(3-k)`
- Adaptive sampling density: more samples on the curve mean smoother output
- Building the resulting polyline with corner vertices via
  [`Add2DVertex`](../Add2DVertex.md)
- Chaining several Bezier segments into one continuous polyline

## Python Script
```python
import vs

kCorner = 0     # vertex type for Add2DVertex


def cubic_bezier(p0, p1, p2, p3, t):
    """Evaluate a cubic Bezier at parameter `t` in [0, 1]."""
    u = 1.0 - t
    b0 = u * u * u
    b1 = 3.0 * u * u * t
    b2 = 3.0 * u * t * t
    b3 = t * t * t
    return (b0 * p0[0] + b1 * p1[0] + b2 * p2[0] + b3 * p3[0],
            b0 * p0[1] + b1 * p1[1] + b2 * p2[1] + b3 * p3[1])


def sample_bezier(p0, p1, p2, p3, samples):
    """Return `samples` (>= 2) points along the Bezier, including endpoints."""
    if samples < 2:
        samples = 2
    step = 1.0 / (samples - 1)
    return [cubic_bezier(p0, p1, p2, p3, i * step) for i in range(samples)]


def draw_control_polygon(p0, p1, p2, p3):
    """Draw the control polygon and drop a locus at each anchor / handle."""
    for a, b in ((p0, p1), (p1, p2), (p2, p3)):
        vs.MoveTo(a[0], a[1])
        vs.LineTo(b[0], b[1])
    for pt in (p0, p1, p2, p3):
        vs.Locus(pt[0], pt[1])


def bezier_polyline(segments, samples_per_segment=24):
    """Concatenate several Bezier segments into a single polyline.

    `segments` is a list of (p0, p1, p2, p3) tuples. Consecutive segments should
    share endpoints (the last p3 of segment N equals the first p0 of segment
    N+1) for a continuous curve.
    """
    vs.BeginPoly()
    for k, (p0, p1, p2, p3) in enumerate(segments):
        pts = sample_bezier(p0, p1, p2, p3, samples_per_segment)
        # Skip the first point of every segment after the first, otherwise
        # we duplicate the shared vertex.
        start = 1 if k > 0 else 0
        for x, y in pts[start:]:
            vs.Add2DVertex(x, y, kCorner, 0)
    vs.EndPoly()
    return vs.LNewObj()


def main():
    # Two Bezier segments chained end-to-end into an "S-curve".
    seg1 = ((0.0, 0.0), (1.5, 0.0), (1.5, 3.0), (3.0, 3.0))
    seg2 = ((3.0, 3.0), (4.5, 3.0), (4.5, 0.0), (6.0, 0.0))

    draw_control_polygon(*seg1)
    draw_control_polygon(*seg2)

    bezier_polyline([seg1, seg2], samples_per_segment=32)

    vs.Message('Two-segment cubic Bezier sampled into a polyline.')

main()
```

## Key VectorScript Functions Used
- [`BeginPoly`](../BeginPoly.md), [`Add2DVertex`](../Add2DVertex.md), [`EndPoly`](../EndPoly.md)
- [`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md)
- [`Locus`](../Locus.md)
- [`LNewObj`](../LNewObj.md), [`Message`](../Message.md)
