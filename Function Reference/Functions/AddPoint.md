# AddPoint

## Description
Procedure AddPoint adds a vertex point to a newly created polygon. AddPoint is designed to be used with BeginPoly and EndPoly to define new polygon objects via VectorScript.

```pascal
PROCEDURE AddPoint(px,py : REAL);
```

```python
def vs.AddPoint(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|px|REAL|X Coordinates of vertex.|
|py|REAL|Y Coordinates of vertex.|

## Examples
#### VectorScript ####
```pascal
BeginPoly;
AddPoint(0,0);
AddPoint(2,0);
AddPoint(2,2);
AddPoint(1,3);
AddPoint(0,2);
AddPoint(0,0);
EndPoly;
{creates a polygon object}

BeginPoly;
AddPoint(x,y);
x := x + 1;
y := y + 1;
AddPoint(x,y);
x:= x + 1;
y := y - 1;
AddPoint(x,y);
EndPoly;
{creates a polygon with vertices as calculated}
```
#### Python ####
```python
vs.BeginPoly()
vs.AddPoint(0,0)
vs.AddPoint(2,0)
vs.AddPoint(2,2)
vs.AddPoint(1,3)
vs.AddPoint(0,2)
vs.AddPoint(0,0)
vs.EndPoly()
#{creates a polygon object}
```

```pascal
3: BEGIN
	AddPoint(Offset,0.0);
	AddPoint(Offset + Scaler*BreakWidth/4,Scaler*BreakHeight/2);
	AddPoint(Offset + Scaler*3*BreakWidth/4,-1*Scaler*BreakHeight/2);
	AddPoint(Offset + Scaler*BreakWidth,0.0);
	END;

BeginXtrd(LeftCabLength-CabThick,LeftCabLength);
BeginPoly;
AddPoint(X,Y);
AddPoint(CabHeight,Y);
AddPoint(CabHeight,Y-CabDepth+FaceThick);
AddPoint(KickHeight,Y-CabDepth+FaceThick);
AddPoint(KickHeight,Y-CabDepth+KickInset+CabThick);

BeginPoly;
	max:=2*PI;
	WHILE CurAng<max DO  BEGIN
		s:=sin(curang);c:=cos(curang);
		AddPoint(iRad*s,iRad*c);
		curAng:=curAng+ang;
	END;
```
```python
# Create poly for roadbed
vs.BeginPoly()
vs.AddPoint( p40 )
vs.AddPoint( p5 )
vs.AddPoint( p6 )
vs.AddPoint( p70 )
vs.EndPoly()

# Draw paving
vs.ClosePoly()
vs.BeginPoly()
vs.AddPoint( p4 )
vs.AddPoint( p3 )
vs.AddPoint( p6 )
vs.AddPoint( p5 )
vs.EndPoly()

vs.MoveTo( 0, 0 )
vs.MoveTo( w, 0 )
vs.ArcTo( w, r1 * vs.Tan( theta / 2 ), 0 )
vs.AddPoint( w + r1 - ( r1 * vs.Cos( theta ) ), r1 * vs.Sin( theta ) )
vs.MoveTo( -( r1 - ( r1 * vs.Cos( theta ) ) ), r1 * vs.Sin( theta ) )
vs.ArcTo( 0, r1 * vs.Tan( theta / 2 ), 0 )
vs.LineTo( 0, 0 )
vs.EndPoly()
```
See also in tutorials: [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md), [12. Polygon Area and Centroid (Shoelace Formula)](ai%20examples/12_PolygonAreaCentroid.md), [13. Point-in-Polygon Test (Ray Casting)](ai%20examples/13_PointInPolygonRayCast.md), [14. Polygon Inward / Outward Offset](ai%20examples/14_PolygonInwardOffset.md)

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
