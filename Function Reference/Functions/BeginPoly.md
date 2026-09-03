# BeginPoly

## Description
Procedures BeginPoly creates a new polygon or polyline object in a VectorWorks document. When used with vertex creation procedure calls, BeginPoly and EndPoly() define the polygon object on a vertex by vertex basis.

A minimum of two vertices must be created, and calculations may be performed within the creation structure between vertex calls, thus allowing additional flexibility in object generation.Hidden edges may be created by using use MoveTo() or Move() between vertex calls.

```pascal
PROCEDURE BeginPoly;
```

```python
def vs.BeginPoly():
    return None
```

## Examples
```pascal
BeginPoly;
```
```python
vs.MoveTo(0,0)
vs.ClosePoly()
vs.BeginPoly()
vs.MoveTo( -0.5 * dMmarkerSize, 0.5 * dMmarkerSize )
vs.ArcTo( 	0,1 * dMmarkerSize, 0 )
vs.LineTo( 	0.5 * dMmarkerSize, 0.5 * dMmarkerSize )
vs.LineTo( 	0,1 * dMmarkerSize )

# Create poly for roadbed
vs.BeginPoly()
vs.AddPoint( p40 )
vs.AddPoint( p5 )
vs.AddPoint( p6 )
vs.AddPoint( p70 )

# Draw paving
vs.ClosePoly()
vs.BeginPoly()
vs.AddPoint( p4 )
vs.AddPoint( p3 )
vs.AddPoint( p6 )
vs.AddPoint( p5 )
```
See also in tutorials: [03. Build a Curved Path with Mixed Vertex Types](ai%20examples/03_CurvedPolylinePath.md), [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md), [12. Polygon Area and Centroid (Shoelace Formula)](ai%20examples/12_PolygonAreaCentroid.md), [13. Point-in-Polygon Test (Ray Casting)](ai%20examples/13_PointInPolygonRayCast.md)

## See Also
<listTable indent="1" cols="4">
[AddPoint](AddPoint.md)
[ArcTo](ArcTo.md)
[BeginPoly](BeginPoly.md)
[ClosePoly](ClosePoly.md)
[CurveThrough](CurveThrough.md)
[CurveTo](CurveTo.md)
[DelVertex](DelVertex.md)
[EndPoly](EndPoly.md)
[GetHole](GetHole.md)
[GetNumHoles](GetNumHoles.md)
[GetPolylineVertex](GetPolylineVertex.md)
[GetPolyPt](GetPolyPt.md)
[GetVertexVisibility](GetVertexVisibility.md)
[GetVertNum](GetVertNum.md)
[InsertVertex](InsertVertex.md)
[OpenPoly](OpenPoly.md)
[Poly](Poly.md)
[SetPolylineVertex](SetPolylineVertex.md)
[SetPolyPt](SetPolyPt.md)
[SetVertexVisibility](SetVertexVisibility.md)
[Smooth](Smooth.md)
</listTable>

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
