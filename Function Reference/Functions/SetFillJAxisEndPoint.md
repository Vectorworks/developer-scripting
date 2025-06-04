# SetFillJAxisEndPoint

## Description
Sets the J-axis end point of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE SetFillJAxisEndPoint(
				objectHandle   : HANDLE;
				xJAxisEndPoint : REAL;
				yJAxisEndPoint : REAL);
```

```python
def vs.SetFillJAxisEndPoint(objectHandle, xJAxisEndPoint, yJAxisEndPoint):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to object with fill.|
|xJAxisEndPoint|REAL|X coordinate of J-axis point.|
|yJAxisEndPoint|REAL|Y coordinate of J-axis point.|

## Examples
==== VectorScript ====
```pascal
SetFillJAxisEndPoint(objectHandle, 15.0, 25.0);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
