# GetFillPoints

## Description
Gets start and axis end points of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE GetFillPoints(
				objectHandle       : HANDLE;
				VAR xOriginPoint   : REAL;
				VAR yOriginPoint   : REAL;
				VAR xIAxisEndPoint : REAL;
				VAR yIAxisEndPoint : REAL;
				VAR xJAxisEndPoint : REAL;
				VAR yJAxisEndPoint : REAL);
```

```python
def vs.GetFillPoints(objectHandle):
    return (xOriginPoint, yOriginPoint, xIAxisEndPoint, yIAxisEndPoint, xJAxisEndPoint, yJAxisEndPoint)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object with fill.|
|xOriginPoint|REAL|X coordinate of origin point.|
|yOriginPoint|REAL|Y coordinate of origin point.|
|xIAxisEndPoint|REAL|X coordinate of I-axis point.|
|yIAxisEndPoint|REAL|Y coordinate of I-axis point.|
|xJAxisEndPoint|REAL|X coordinate of J-axis point.|
|yJAxisEndPoint|REAL|Y coordinate of J-axis point.|

## Examples
==== VectorScript ====
```pascal
GetFillPoints(objectHandle);
```
==== Python ====
```python
xOrigin, yOrigin, xIAxis, yIAxis, xJAxis, yJAxis = vs.GetFillPoints(vs.FSActLayer())
```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
