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

```pascal
GetFillOriginPoint(objectHandle, 1.0, 2.0);
```
```python
import vs

# Gets the origin point of the fill.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

xOriginPoint, yOriginPoint = vs.GetFillOriginPoint(objectHandle)
vs.Message('GetFillOriginPoint returned: ' + str((xOriginPoint, yOriginPoint)))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
