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
