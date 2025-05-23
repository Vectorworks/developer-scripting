# NurbsCurveGetNumPieces

## Description
Returns the number of pieces that compose the referenced NURBS curve.

```pascal
FUNCTION NurbsCurveGetNumPieces(objectHd : HANDLE): INTEGER;
```

```python
def vs.NurbsCurveGetNumPieces(objectHd):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve.|

## Remarks
See example on [[VS:NurbsGetPt3D]]

## Examples
presentation of pieces (segments in the example) in a NURBS curve:

[[File:NURBS_Pieces.png| 500px]]

## Version
Availability: from VectorWorks 9.0

## Category
* Objects - NURBS

