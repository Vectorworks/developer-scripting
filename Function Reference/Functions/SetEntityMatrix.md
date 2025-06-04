# SetEntityMatrix

## Description
Sets the matrix of the plane for a planar object. If there is already a plane in the document with that matrix, the object will be set to be in that plane. Otherwise a new plane will be added to the document.

```pascal
FUNCTION SetEntityMatrix(
				objectHandle   : HANDLE;
				offsetX        : REAL;
				offsetY        : REAL;
				offsetZ        : REAL;
				rotationXAngle : REAL;
				rotationYAngle : REAL;
				rotationZAngle : REAL): BOOLEAN;
```

```python
def vs.SetEntityMatrix(objectHandle, offset, rotationXAngle, rotationYAngle, rotationZAngle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object whose plane is being set.|
|offset|REAL|The X, Y and Z offsets of the plane in current document units.|
|rotationXAngle|REAL|The rotation of the plane about the X-axis in degrees.|
|rotationYAngle|REAL|The rotation of the plane about the Y-axis in degrees.|
|rotationZAngle|REAL|The rotation of the plane about the Z-axis in degrees.|

## Version
Availability: from Vectorworks 2011

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
