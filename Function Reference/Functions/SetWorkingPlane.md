# SetWorkingPlane

## Description
Sets the x, y, and z offset of the working plane as well as the x-, y-, and z-plane rotational values.

```pascal
PROCEDURE SetWorkingPlane(
				x         : REAL;
				y         : REAL;
				z         : REAL;
				xRotation : REAL;
				yRotation : REAL;
				zRotation : REAL);
```

```python
def vs.SetWorkingPlane(x, y, z, xRotation, yRotation, zRotation):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x|REAL|X-coordinate of the working plane|
|y|REAL|Y-coordinate of the working plane|
|z|REAL|Z-coordinate of the working plane|
|xRotation|REAL|X-coordinate of the rotation|
|yRotation|REAL|Y-coordinate of the rotation|
|zRotation|REAL|Z-coordinate of the rotation|

## Remarks
(\_c\_ 2022.05.12): From Raymond Mullin: as of VW 2022 any working plane set with this routine doesn't persist after script's end. This routine works in this fashion since VW 2011.

## Examples
```pascal
SetWorkingPlane(1.0, 2.0, 0.5, 1.5, 3.0, 1.0);
```
```python
import vs

# Sets the x, y, and z offset of the working plane as well as the x-, y-, and
# z-plane rotational values.
x = 0.0
y = 0.0
z = 0.0
xRotation = 1.0
yRotation = 2.0
zRotation = 0.0

vs.SetWorkingPlane(x, y, z, xRotation, yRotation, zRotation)
```

## See Also
VS Functions:
[GetWorkingPlane](GetWorkingPlane.md)

## Version
Availability: from VectorWorks 10.0

## Category
* [Utility](../Categories/Utility.md)
