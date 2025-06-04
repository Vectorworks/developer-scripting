# ArcTo

## Description
Procedure ArcTo creates an arc vertex with a point of intersection at the specified coordinate point.

The endpoints of the arc are tangent to the control segments which intersect at p. If a radius of 0 is passed as the parameter, the arc endpoints will be at the vertices preceding and following the arc spline vertex.

```pascal
PROCEDURE ArcTo(
				pX,pY          : REAL;
				radiusDistance : REAL);
```

```python
def vs.ArcTo(p, radiusDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinates of vertex.|
|radiusDistance|REAL|Radius of vertex arc.|

## Examples
#### VectorScript ####
```pascal
BeginPoly;
LineTo(-1&quot;,2&quot;);
LineTo(-2 1/2&quot;,1/2&quot;);
CurveTo(-1 1/2&quot;,-1 1/2&quot;);
LineTo(1&quot;,-1/2&quot;);
ArcTo(1&quot;,1 1/2&quot;,1/2&quot;);
EndPoly;
{creates a polyline object}
```
#### Python ####
```python
vs.BeginPoly()
vs.LineTo(-1,2)
vs.LineTo(-2*12 - 1/2,1/2)
vs.CurveTo(-1*12 - 1/2,-1*12 - 1/2)
vs.LineTo(1,-1/2)
vs.ArcTo(1,1*12 + 1/2,1/2)
vs.EndPoly()
#{creates a polyline object}
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
Availability: from MiniCAD4.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
