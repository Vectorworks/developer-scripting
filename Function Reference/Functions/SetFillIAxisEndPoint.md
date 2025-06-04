# SetFillIAxisEndPoint

## Description
Sets the I-axis end point of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE SetFillIAxisEndPoint(
				objectHandle   : HANDLE;
				xIAxisEndPoint : REAL;
				yIAxisEndPoint : REAL);
```

```python
def vs.SetFillIAxisEndPoint(objectHandle, xIAxisEndPoint, yIAxisEndPoint):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object with fill.|
|xIAxisEndPoint|REAL|X coordinate of I-axis point.|
|yIAxisEndPoint|REAL|Y coordinate of I-axis point.|

## Examples
==== VectorScript ====
```pascal
SetFillIAxisEndPoint(objectHandle, 20.0, 10.0);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
