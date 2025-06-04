# CreateInterpolatedSurface

## Description
Creates an interpolated surface with the specified degrees and number of points.  The resulting surface passes through each of the interpoliation points.  If a handle to a NURBS surface is provided, the interpolated surface will approximate that surface.  If the handle is NULL, it creates a rectangular surface.

```pascal
FUNCTION CreateInterpolatedSurface(
				surfaceHandle : HANDLE;
				numUPts       : LONGINT;
				numVPts       : LONGINT;
				uDegree       : INTEGER;
				vDegree       : INTEGER): HANDLE;
```

```python
def vs.CreateInterpolatedSurface(surfaceHandle, numUPts, numVPts, uDegree, vDegree):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|surfaceHandle|HANDLE|Handle to a NURBS surface to approximate|
|numUPts|LONGINT|Number of interpolation points in the U parametric direction.  Must be greater than uDegree.|
|numVPts|LONGINT|Number of interpolation points in the V parametric direction.  Must be greater than vDegree.|
|uDegree|INTEGER|Degree of the surface in the u parametric direction|
|vDegree|INTEGER|Degree of the surface in the v parametric direction|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
