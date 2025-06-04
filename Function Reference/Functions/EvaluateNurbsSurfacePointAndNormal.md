# EvaluateNurbsSurfacePointAndNormal

## Description
Determines the point and normal on the NURBS surface at the given u/v value.

```pascal
FUNCTION EvaluateNurbsSurfacePointAndNormal(
				surfaceHandle               : HANDLE;
				u                           : REAL;
				v                           : REAL;
				VAR pointX,pointY,pointZ    : REAL;
				VAR normalX,normalY,normalZ : REAL): BOOLEAN;
```

```python
def vs.EvaluateNurbsSurfacePointAndNormal(surfaceHandle, u, v):
    return (BOOLEAN, point, normal)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|surfaceHandle|HANDLE|Handle to NURBS surface being evaluated|
|u|REAL|parameter value of the point on the surface being evaluated|
|v|REAL|parameter value of the point on the surface being evaluated|
|point|REAL|Coordinate of the point on the surface|
|normal|REAL|normal vector of the surface computed at the point|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
