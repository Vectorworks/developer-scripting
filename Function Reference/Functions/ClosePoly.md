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
