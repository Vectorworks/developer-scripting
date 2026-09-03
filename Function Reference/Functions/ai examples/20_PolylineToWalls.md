# 20. Read a Polyline and Build Walls Along Its Path

## Description
Reads the vertices of an existing polyline (or falls back to a hardcoded path
when nothing is selected) and materialises a run of straight walls along it.
This is a stripped-down version of the "Poly2Walls" tool in
`Common/Includes/Poly2Walls.px`.

Two side-effects worth noting:
- The wall class is created on the fly with
  [`NameClass`](../NameClass.md).
- Each wall's height is set uniformly through
  [`SetWallOverallHeights`](../SetWallOverallHeights.md),
  and the ends are auto-cut so consecutive walls miter cleanly.

## What This Demonstrates
- Picking up the active selection with
  [`FSActLayer`](../FSActLayer.md)
- Detecting object type (polygon vs polyline) with
  [`GetTypeN`](../GetTypeN.md)
- Reading vertices from a polygon via
  [`GetVertNum`](../GetVertNum.md) +
  [`GetPolyPt`](../GetPolyPt.md)
- Reading vertices from a polyline via
  [`GetPolylineVertex`](../GetPolylineVertex.md)
- Producing walls with [`Wall`](../Wall.md) and grabbing the
  handle each time with [`LNewObj`](../LNewObj.md)

## Python Script
```python
import vs

# Object-type codes used below (see ObjsType.py in Common/Includes).
kTypePolygon  = 5
kTypePolyline = 21


def read_polygon_vertices(hPoly):
    """Read (x, y) tuples from a polygon object."""
    count = vs.GetVertNum(hPoly)
    verts = []
    for i in range(1, count + 1):
        # In Python vs.GetPolyPt returns a (x, y) tuple.
        pt = vs.GetPolyPt(hPoly, i)
        verts.append((pt[0], pt[1]))
    return verts


def read_polyline_vertices(hPoly):
    """Read (x, y) tuples from a polyline. Ignores vertex type/radius here."""
    count = vs.GetVertNum(hPoly)
    verts = []
    for i in range(1, count + 1):
        # GetPolylineVertex returns (px, py, vertexType, arcRadius).
        result = vs.GetPolylineVertex(hPoly, i)
        px, py = result[0], result[1]
        verts.append((px, py))
    return verts


def path_from_handle(h):
    """Return the vertex list for a polygon or polyline, or [] otherwise."""
    if h is None:
        return []
    t = vs.GetTypeN(h)
    if t == kTypePolygon:
        return read_polygon_vertices(h)
    if t == kTypePolyline:
        return read_polyline_vertices(h)
    return []


def walls_along_path(vertices, wallHeight=2.7, className='Walls-Path'):
    """Build one wall per edge of `vertices`. Returns the wall handles."""
    if len(vertices) < 2:
        return []
    vs.NameClass(className)
    handles = []
    for i in range(len(vertices) - 1):
        ax, ay = vertices[i]
        bx, by = vertices[i + 1]
        vs.Wall(ax, ay, bx, by)
        h = vs.LNewObj()
        vs.SetWallOverallHeights(h, 0, 0, '', wallHeight,
                                 0, 0, '', wallHeight)
        vs.WallCap(False, False, False, 0, 0)
        handles.append(h)
    return handles


def main():
    hSel = vs.FSActLayer()
    path = path_from_handle(hSel)

    if not path:
        # No suitable selection: use a demo path so the script still produces output.
        path = [(0.0, 0.0), (6.0, 0.0), (6.0, 3.0), (2.0, 3.0), (2.0, 5.0)]

    walls = walls_along_path(path, wallHeight=2.7)
    vs.Message(str(len(walls)) + ' walls built along a '
               + str(len(path)) + '-vertex path.')

main()
```

## Key VectorScript Functions Used
- [`Wall`](../Wall.md), [`SetWallOverallHeights`](../SetWallOverallHeights.md), [`WallCap`](../WallCap.md)
- [`LNewObj`](../LNewObj.md), [`FSActLayer`](../FSActLayer.md), [`GetTypeN`](../GetTypeN.md)
- [`GetVertNum`](../GetVertNum.md), [`GetPolyPt`](../GetPolyPt.md), [`GetPolylineVertex`](../GetPolylineVertex.md)
- [`NameClass`](../NameClass.md), [`Message`](../Message.md)
