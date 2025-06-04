# NurbsGetWeight

## Description
Returns the weight of a point in a NURBS curve or surface.

For NURBS curves, index1 corresponds to the segment of the curve to be queried, and index2 corresponds to the index of the point in the segment.

For NURBS surfaces, index1 corresponds to the u-index and index2 corresponds to the v-index of the surface.

The index is zero based (0 to number of points - 1).

```pascal
PROCEDURE NurbsGetWeight(
				objectHd   : HANDLE;
				index1     : LONGINT;
				index2     : LONGINT;
				VAR weight : REAL);
```

```python
def vs.NurbsGetWeight(objectHd, index1, index2):
    return weight
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index1|LONGINT|Segment of curve to be queried (NURBS curve), or u-index (NURBS surface).|
|index2|LONGINT|Index of point (NURBS curve) or v-index (NURBS surface).|
|weight|REAL|Weight of point.|

## Remarks
this function will work for both nurbs curves and nurbs surfaces.

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
