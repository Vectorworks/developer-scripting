# 15. Uniform Arc-Length Resampling of a Polyline

## Description
Takes any open polyline given as a list of vertices and returns a new list where
the vertices are spaced at uniform arc length. This is useful when you need to
place features (posts, plants, fasteners) at regular intervals along a path
that was drawn freehand or imported from GIS.

## What This Demonstrates
- Computing edge lengths and cumulative arc length along a polyline
- Interpolating a point at a given arc length by walking the edges
- Two use-cases for the result:
  1. redrawing the polyline as a smoother uniformly-sampled version, and
  2. placing loci at each sample as if they were fence posts

## Python Script
```python
import math
import vs


def edge_lengths(vertices):
    """Return the length of each edge and the total polyline length."""
    lengths = []
    for i in range(len(vertices) - 1):
        x1, y1 = vertices[i]
        x2, y2 = vertices[i + 1]
        lengths.append(math.hypot(x2 - x1, y2 - y1))
    return lengths, sum(lengths)


def point_at_arclength(vertices, edge_lens, s):
    """Return the point at arc-length `s` measured from vertices[0]."""
    if s <= 0.0:
        return vertices[0]
    accum = 0.0
    for i, edge in enumerate(edge_lens):
        if accum + edge >= s:
            t = 0.0 if edge < 1e-12 else (s - accum) / edge
            x1, y1 = vertices[i]
            x2, y2 = vertices[i + 1]
            return (x1 + t * (x2 - x1), y1 + t * (y2 - y1))
        accum += edge
    return vertices[-1]


def resample_polyline(vertices, sample_count):
    """Return `sample_count` points spaced uniformly along the polyline.

    The first and last samples always coincide with the polyline's endpoints.
    """
    if sample_count < 2 or len(vertices) < 2:
        return list(vertices)
    edge_lens, total = edge_lengths(vertices)
    if total < 1e-12:
        return [vertices[0]] * sample_count
    step = total / (sample_count - 1)
    return [point_at_arclength(vertices, edge_lens, i * step)
            for i in range(sample_count)]


def draw_open_polyline(vertices):
    """Emit `vertices` as an open polygon-like polyline for visualization."""
    for i in range(len(vertices) - 1):
        x1, y1 = vertices[i]
        x2, y2 = vertices[i + 1]
        vs.MoveTo(x1, y1)
        vs.LineTo(x2, y2)


def main():
    # A jaggy path — few vertices, wildly varying segment lengths.
    path = [
        (0.0, 0.0), (1.0, 0.5), (1.5, 2.0), (3.5, 2.2),
        (4.0, 0.8), (6.0, 1.0), (7.5, 3.0), (9.5, 3.0),
    ]

    # 1. Draw the raw path.
    draw_open_polyline(path)

    # 2. Resample into 20 equally-spaced points and draw them offset by 4 in Y.
    samples = resample_polyline(path, 20)
    lifted = [(x, y + 4.0) for (x, y) in samples]
    draw_open_polyline(lifted)

    # 3. Drop a locus at every sample so you can see the spacing.
    for pt in lifted:
        vs.Locus(pt[0], pt[1])

    _, total = edge_lengths(path)
    vs.Message('Path length = ' + vs.Num2Str(3, total)
               + ' | samples = ' + str(len(samples)))

main()
```

## Key VectorScript Functions Used
- [`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md)
- [`Locus`](../Locus.md)
- [`Num2Str`](../Num2Str.md), [`Message`](../Message.md)
- Related: [`GetPolyPt`](../GetPolyPt.md) / [`GetPolylineVertex`](../GetPolylineVertex.md) to read vertices from existing polylines
