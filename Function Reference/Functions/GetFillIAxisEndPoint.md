# GetFillIAxisEndPoint

## Description
Gets the I-axis end point of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE GetFillIAxisEndPoint(
				objectHandle       : HANDLE;
				VAR xIAxisEndPoint : REAL;
				VAR yIAxisEndPoint : REAL);
```

```python
def vs.GetFillIAxisEndPoint(objectHandle):
    return (xIAxisEndPoint, yIAxisEndPoint)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object with fill.|
|xIAxisEndPoint|REAL|X coordinate of I-axis point.|
|yIAxisEndPoint|REAL|Y coordinate of I-axis point.|

## Examples
#### VectorScript ####
```pascal
GetFillIAxisEndPoint(objectHandle, xIAxis, yIAxis);
```
#### Python ####
```python
xIAxis, yIAxis = vs.GetFillIAxisEndPoint(vs.FSActLayer())
```

```pascal
GetFillIAxisEndPoint(objectHandle, 1.0, 2.0);
```
```python
import vs

# Gets the I-axis end point of the fill.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

xIAxisEndPoint, yIAxisEndPoint = vs.GetFillIAxisEndPoint(objectHandle)
vs.Message('GetFillIAxisEndPoint returned: ' + str((xIAxisEndPoint, yIAxisEndPoint)))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
