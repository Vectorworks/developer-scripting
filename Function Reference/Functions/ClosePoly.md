# ClosePoly

## Description
Procedures ClosePoly set the polygon creation mode for polygon objects created in VectorScript to closed. To turn this mode off, use Procedure OpenPoly; the two modes used in conjunction will act as a toggle for the feature.

```pascal
PROCEDURE ClosePoly;
```

```python
def vs.ClosePoly():
    return None
```

## Examples
#### VectorScript ####
```pascal
ClosePoly;
Poly(0,0,1,1,1,-1);
{creates a closed 3 sided polygon}
```
#### Python ####
```python
vs.ClosePoly()
vs.Poly(0,0,1,1,1,-1)
#{creates a closed 3 sided polygon}
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
