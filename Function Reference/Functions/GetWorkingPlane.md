# GetWorkingPlane

## Description
Retrieves the location and orientation of the working plane.

```pascal
PROCEDURE GetWorkingPlane(
				VAR x         : REAL;
				VAR y         : REAL;
				VAR z         : REAL;
				VAR xRotation : REAL;
				VAR yRotation : REAL;
				VAR zRotation : REAL);
```

```python
def vs.GetWorkingPlane():
    return (x, y, z, xRotation, yRotation, zRotation)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x|REAL|X-coordinate of the working plane|
|y|REAL|Y-coordinate of the working plane|
|z|REAL|Z-coordinate of the working plane|
|xRotation|REAL|X-coordinate value of the rotation|
|yRotation|REAL|Y-coordinate value of the rotation|
|zRotation|REAL|Z-coordinate value of the rotation|

## See Also
VS Functions:
[SetWorkingPlane](SetWorkingPlane.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Utility](../Categories/Utility.md)
