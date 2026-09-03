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

## Examples
```pascal
resultH := ExtendNurbsCurve(curveHandle, 1.0, TRUE, FALSE);
```
```python
import vs

# Extends a curve by a given distance at the start or the end.
curveHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
distance = 1.0
bStart = True
bLinear = True

objHandle = vs.ExtendNurbsCurve(curveHandle, distance, bStart, bLinear)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
