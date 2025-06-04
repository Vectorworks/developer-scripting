# NurbsDegree

## Description
Returns the degree of a segment in a NURBS curve or surface.

For NURBS curves, the index indicates which segment of the curve is to be queried. The index is zero based (0 to number of segments - 1).

For NURBS surfaces, specify an index of 1 to indicate u-direction, and an index of 0 to indicate v-direction when querying the surface object.

```pascal
FUNCTION NurbsDegree(
				objectHd : HANDLE;
				index    : INTEGER): INTEGER;
```

```python
def vs.NurbsDegree(objectHd, index):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index|INTEGER|Index of curve segment (NURBS curve) or direction index (NURBS surface).|

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
