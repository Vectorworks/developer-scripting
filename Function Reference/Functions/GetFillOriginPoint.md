# GetFillOriginPoint

## Description
Gets the origin point of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE GetFillOriginPoint(
				objectHandle     : HANDLE;
				VAR xOriginPoint : REAL;
				VAR yOriginPoint : REAL);
```

```python
def vs.GetFillOriginPoint(objectHandle):
    return (xOriginPoint, yOriginPoint)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object with fill.|
|xOriginPoint|REAL|X coordinate of origin point.|
|yOriginPoint|REAL|Y coordinate of origin point.|

## Examples
#### VectorScript ####
```pascal
GetFillOriginPoint(objectHandle, xOrigin, yOrigin);
```
#### Python ####
```python
xIAxis, yIAxis = vs.GetFillOriginPoint(vs.FSActLayer())
```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
