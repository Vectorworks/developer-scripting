# Get3DOrientation

## Description
Function Get3DOrientation returns the 3D orientation of the referenced object.

If the object is mirrored, a reflection across the X-Y plane must be applied before rotating by the angles above in order to reproduce the object's orientation.

```pascal
FUNCTION Get3DOrientation(
				h                : HANDLE;
				VAR xRot         : REAL;
				VAR yRot         : REAL;
				VAR zRot         : REAL;
				VAR isMirroredXY : BOOLEAN): BOOLEAN;
```

```python
def vs.Get3DOrientation(h):
    return (BOOLEAN, xRot, yRot, zRot, isMirroredXY)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to 3D object.|
|xRot|REAL|Returns X rotation value.|
|yRot|REAL|Returns Y rotation value.|
|zRot|REAL|Returns Z rotation value.|
|isMirroredXY|BOOLEAN|Returns mirror status of object.|

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
