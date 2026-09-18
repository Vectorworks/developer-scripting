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

## Examples
```pascal
BEGIN
temp_i := 0;
temp_h := fingroup(groupH);
IF Get3DOrientation(temp_h,rotx,roty,rotz,temp_b) THEN BEGIN
	IF kDebugMode THEN alrtdialog(concat('The selected item has rotation values of ',num2str(2,rotx),',',num2str(2,roty),',',num2str(2,rotz),'.'));
	CASE Trunc(rotx) OF
	-89,-90:CASE Trunc(roty) OF
		-89,-90: temp_i := 3;
		0: temp_i := 2;

getsymloc3d(hs,x,y,z);
gflag := Get3DOrientation(hs,xr,yr,zr,flip);

GetSymLoc3D (ghParm,BumpLocX,BumpLocY,BumpLocZ);
BoxRot := GetSymRot (ghParm);
gBumperRot := getSymRot (ghParm);
Got3D := Get3DOrientation (ghParm, Orient3DX, Orient3DY, Orient3DZ, PIOMirrored);
```
```python
import vs

# Function Get3DOrientation returns the 3D orientation of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, xRot, yRot, zRot, isMirroredXY = vs.Get3DOrientation(h)
vs.Message('Get3DOrientation returned: ' + str((ok, xRot, yRot, zRot, isMirroredXY)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
