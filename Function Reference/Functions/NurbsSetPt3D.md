# NurbsSetPt3D

## Description
Sets the coordinates of a point in the referenced NURBS curve or surface.

The index is zero based (0 to number of points - 1).

For a nurbs curve, index1 is the piece number of the nurbs curve. Index2 is the vertex number within that piece. NurbsCurveGetNumPieces will give you the number of pieces inside of the nurbs curve (1-based). NurbsGetNumPts will give you the number of points inside of a piece.

```pascal
PROCEDURE NurbsSetPt3D(
				objectHd : HANDLE;
				index1   : LONGINT;
				index2   : LONGINT;
				pX,pY,pZ : REAL);
```

```python
def vs.NurbsSetPt3D(objectHd, index1, index2, p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index1|LONGINT|Index of point in NURBS curve, or u-coordinate of point location in NURBS surface.|
|index2|LONGINT|V-coordinate of point location in NURBS surface.|
|p|REAL|New coordinates for the point.|

## Remarks
this function will work for both nurbs curves and nurbs surfaces.

set the indexed vertex of the indexed point of the given nurbs curve or the indexed (index2)control point of the surfaces in either the U (index 1= 1)or V(index1 =0) direction

## Examples
==== VectorScript ====
```pascal
See NurbsSurfaceEvalPt
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
