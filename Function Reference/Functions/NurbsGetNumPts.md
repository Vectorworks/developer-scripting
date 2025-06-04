# NurbsGetNumPts

## Description
Returns the number of points for segment of the referenced NURBS curve, or the number of points of the referenced NURBS surface in the u- or v-direction.

For NURBS curves, the index indicates which segment of the curve is to be queried. The index is zero based (0 to number of segments - 1).

For NURBS surfaces, specify an index of 1 to indicate u-direction, and an index of 0 to indicate v-direction when querying the surface object.

```pascal
FUNCTION NurbsGetNumPts(
				objectHd : HANDLE;
				index    : LONGINT): LONGINT;
```

```python
def vs.NurbsGetNumPts(objectHd, index):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index|LONGINT|Index of curve segment (NURBS curve) or direction index (NURBS surface).|

## Remarks
this function will work for both nurbs curves and nurbs surfaces.

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
