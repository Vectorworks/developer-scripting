# GetSymLoc3D

## Description
Determines the location of a specified symbol or plug-in object in 3D space.

```pascal
PROCEDURE GetSymLoc3D(
				objectHandle : HANDLE;
				VAR x        : REAL;
				VAR y        : REAL;
				VAR z        : REAL);
```

```python
def vs.GetSymLoc3D(objectHandle):
    return (x, y, z)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to a symbol instance or a plug-in object in the drawing.|
|x|REAL|The location of the object along the x-axis.|
|y|REAL|The location of the object along the y-axis.|
|z|REAL|The location of the object along the z-axis.|

## Examples
```pascal
BEGIN
  Symbol(KnobName,X1+DoorWidth/2,Y1-DoorHeight/2,90);
  GetSymLoc3D(lNewObj,xctr,yctr,zctr);
  SET3DRot(lNewObj, 0, 90, 0, xctr,yctr,zctr);
END;

BEGIN
	SymDefName := GetSymName(ObjH);
	SymObjClass := GetClass(ObjH);
	GetSymLoc3D(ObjH,xLoc,yLoc,zLoc);
	GetSymLoc(ObjH,xLoc,yLoc);
	SymRot := GetSymRot(ObjH);
	DelObj(ObjH);
	END;

{get obj position and rotation}
GetSymLoc3D( objectHand, locX, locY, locZ );
rot		:= GetSymRot( objectHand );
```
```python
import vs

# Determines the location of a specified symbol or plug-in object in 3D space.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

x, y, z = vs.GetSymLoc3D(objectHandle)
vs.Message('GetSymLoc3D returned: ' + str((x, y, z)))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
