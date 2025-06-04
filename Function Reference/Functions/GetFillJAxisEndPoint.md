# GetFillJAxisEndPoint

## Description
Gets the J-axis end point of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE GetFillJAxisEndPoint(
				objectHandle       : HANDLE;
				VAR xJAxisEndPoint : REAL;
				VAR yJAxisEndPoint : REAL);
```

```python
def vs.GetFillJAxisEndPoint(objectHandle):
    return (xJAxisEndPoint, yJAxisEndPoint)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object with fill.|
|xJAxisEndPoint|REAL|X coordinate of J-axis point.|
|yJAxisEndPoint|REAL|Y coordinate of J-axis point.|

## Examples
#### VectorScript ####
```pascal
GetFillJAxisEndPoint(objectHandle, xJAxis, yJAxis);
```
#### Python ####
```python
xIAxis, yIAxis = vs.GetFillJAxisEndPoint(vs.FSActLayer())
```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
