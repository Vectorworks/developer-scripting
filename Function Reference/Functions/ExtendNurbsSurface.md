# ExtendNurbsSurface

## Description
Extends a surface by a given distance at the start or the end of the U direction or V direction.

```pascal
FUNCTION ExtendNurbsSurface(
				surfaceHandle : HANDLE;
				distance      : REAL;
				bStart        : BOOLEAN;
				bLinear       : BOOLEAN;
				bUDir         : BOOLEAN): HANDLE;
```

```python
def vs.ExtendNurbsSurface(surfaceHandle, distance, bStart, bLinear, bUDir):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|surfaceHandle|HANDLE|Handle to a NURBS surface.|
|distance|REAL|Distance to extend the surface.|
|bStart|BOOLEAN|True to extend from the beginning, false to extend from the end.|
|bLinear|BOOLEAN|True for linear, false to match curvature of existing surface.|
|bUDir|BOOLEAN|True extends the surface in the u parametric|direction, otherwise extends it in the v parametric direction.|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
