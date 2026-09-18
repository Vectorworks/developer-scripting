# EndPoly

## Description
Procedure EndPoly completes the definition of a polygon or polyline object within a VectorWorks document. On calling EndPoly, the object is created in the document from the preceding vertex creation calls.

```pascal
PROCEDURE EndPoly;
```

```python
def vs.EndPoly():
    return None
```

## Examples
```pascal
EndPoly;
```
```python
vs.ArcTo( 	0,1 * dMmarkerSize, 0 )
vs.LineTo( 	0.5 * dMmarkerSize, 0.5 * dMmarkerSize )
vs.LineTo( 	0,1 * dMmarkerSize )
vs.EndPoly()
vs.MoveTo ( 0,1.5 	* dMmarkerSize )

vs.AddPoint( p5 )
vs.AddPoint( p6 )
vs.AddPoint( p70 )
vs.EndPoly()

vs.AddPoint( p3 )
vs.AddPoint( p6 )
vs.AddPoint( p5 )
vs.EndPoly()
SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gPaving_Class, vs.PShow_Joints)
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
