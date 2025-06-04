# NurbsNumKnots

## Description
Returns the number of knots for the referenced NURBS curve or surface. If the object is a curve, then index indicates the segment of the curve to consider. If the object is a surface, then the index indicates the U direction (for index = 1) or the V direction (for index = 0).

```pascal
FUNCTION NurbsNumKnots(
				objectHd : HANDLE;
				index    : LONGINT): LONGINT;
```

```python
def vs.NurbsNumKnots(objectHd, index):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index|LONGINT|Index of curve, or U/V choice for surface.|

## Remarks
/this function will work for both nurbs curves and nurbs surfaces.
returns the number of knots for the indexed piece of the given nurbs curve.  or number of U knot vector (index=1) or V knot vector (index=0) of the given nurbs surface

## Examples
#### VectorScript ####
```pascal
See NurbsSurfaceEvalPt
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
