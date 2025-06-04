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

## See Also
<listTable indent="1" cols="4">
[AddPoint|AddPoint](AddPoint|AddPoint.md)
[ArcTo|ArcTo](ArcTo|ArcTo.md)
[BeginPoly|BeginPoly](BeginPoly|BeginPoly.md)
[ClosePoly|ClosePoly](ClosePoly|ClosePoly.md)
[CurveThrough|CurveThrough](CurveThrough|CurveThrough.md)
[CurveTo|CurveTo](CurveTo|CurveTo.md)
[DelVertex|DelVertex](DelVertex|DelVertex.md)
[EndPoly|EndPoly](EndPoly|EndPoly.md)
[GetHole|GetHole](GetHole|GetHole.md)
[GetNumHoles|GetNumHoles](GetNumHoles|GetNumHoles.md)
[GetPolylineVertex|GetPolylineVertex](GetPolylineVertex|GetPolylineVertex.md)
[GetPolyPt|GetPolyPt](GetPolyPt|GetPolyPt.md)
[GetVertexVisibility|GetVertexVisibility](GetVertexVisibility|GetVertexVisibility.md)
[GetVertNum|GetVertNum](GetVertNum|GetVertNum.md)
[InsertVertex|InsertVertex](InsertVertex|InsertVertex.md)
[OpenPoly|OpenPoly](OpenPoly|OpenPoly.md)
[Poly|Poly](Poly|Poly.md)
[SetPolylineVertex|SetPolylineVertex](SetPolylineVertex|SetPolylineVertex.md)
[SetPolyPt|SetPolyPt](SetPolyPt|SetPolyPt.md)
[SetVertexVisibility|SetVertexVisibility](SetVertexVisibility|SetVertexVisibility.md)
[Smooth|Smooth](Smooth|Smooth.md)
</listTable>

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
