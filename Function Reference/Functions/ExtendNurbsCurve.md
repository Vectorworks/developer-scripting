# ExtendNurbsCurve

## Description
Extends a curve by a given distance at the start or the end.  The extension can either be linear or can match the curvature of the existing end.

```pascal
FUNCTION ExtendNurbsCurve(
				curveHandle : HANDLE;
				distance    : REAL;
				bStart      : BOOLEAN;
				bLinear     : BOOLEAN): HANDLE;
```

```python
def vs.ExtendNurbsCurve(curveHandle, distance, bStart, bLinear):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|curveHandle|HANDLE|Handle to a NURBS curve|
|distance|REAL|Distance to extend the curve|
|bStart|BOOLEAN|True to extend the curve at the beginning, false to extend it at the end.|
|bLinear|BOOLEAN|True for linear, false to match curvature of existing end.|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
