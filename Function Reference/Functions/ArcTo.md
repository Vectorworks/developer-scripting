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

```pascal
BEGIN
	IF r[i] > 0 THEN
		ArcTo(x0 + x[i],y0 + y[i],r[i])
	ELSE
		LineTo(x0 + x[i], y0 + y[i]);
END;

CASE vertexTypeFlag OF
	0 : LineTo (vertexX, #vertexY);
	1 : CurveTo (vertexX, #vertexY);
	2 : CurveThrough (vertexX, #vertexY);
	3 : ArcTo (vertexX, #vertexY, 0);
END;

2: BEGIN
	ArcTo(Offset,0.0,Scaler*BreakRad);
	AddPoint(Offset + Scaler*BreakWidth/4,Scaler*BreakHeight/2);
	AddPoint(Offset + Scaler*3*BreakWidth/4,-1*Scaler*BreakHeight/2);
	ArcTo(Offset + Scaler*BreakWidth,0.0,Scaler*BreakRad);
	END;
```
```python
vs.ClosePoly()
vs.BeginPoly()
vs.MoveTo( -0.5 * dMmarkerSize, 0.5 * dMmarkerSize )
vs.ArcTo( 	0,1 * dMmarkerSize, 0 )
vs.LineTo( 	0.5 * dMmarkerSize, 0.5 * dMmarkerSize )
vs.LineTo( 	0,1 * dMmarkerSize )
vs.EndPoly()
vs.MoveTo ( 0,1.5 	* dMmarkerSize )

vs.BeginPoly()
vs.MoveTo( 0, 0 )
vs.MoveTo( -distance, 0 )
vs.ArcTo( 0, e, r2 )
vs.LineTo( f * vs.Sin( theta ), f * vs.Cos( theta ) )
vs.MoveTo( distance * vs.Cos( theta ), -distance * vs.Sin( theta ) )
vs.ArcTo( -b * vs.Sin( theta ), -b * vs.Cos( theta ), r1 )
vs.LineTo( 0, -a )

vs.BeginPoly()
vs.MoveTo( 0, 0 )
vs.MoveTo( w, 0 )
vs.ArcTo( w, r1 * vs.Tan( theta / 2 ), 0 )
vs.AddPoint( w + r1 - ( r1 * vs.Cos( theta ) ), r1 * vs.Sin( theta ) )
vs.MoveTo( -( r1 - ( r1 * vs.Cos( theta ) ) ), r1 * vs.Sin( theta ) )
vs.ArcTo( 0, r1 * vs.Tan( theta / 2 ), 0 )
vs.LineTo( 0, 0 )
```

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
Availability: from MiniCAD4.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
