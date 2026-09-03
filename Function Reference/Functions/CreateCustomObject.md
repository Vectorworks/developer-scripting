# CreateCustomObject

## Description
Creates a custom object instance at the specified location and angle of rotation. For the objectName, use the &quot;internal&quot; plug-in name (the one assigned in the plug-in editor), as opposed to the filename (which can be different).

```pascal
FUNCTION CreateCustomObject(
				objectName    : STRING;
				pX,pY         : REAL;
				rotationAngle : REAL): HANDLE;
```

```python
def vs.CreateCustomObject(objectName, p, rotationAngle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Name of object.|
|p|REAL|Insertion point of object instance.|
|rotationAngle|REAL|Rotation angle (in degrees) of object instance.|

## Remarks
Like for objects created through CreateCustomObjectPath, they don't resolve as "new objects" after creation with this routine.

## Examples
```pascal
	BEGIN
	planRotation := GetPrefReal( 93 );
	plantRoatation := GetSymRot(key_plant);
	FOR i := 1 TO plant_loc_num DO BEGIN
		temp_h := createcustomobject('Plant',plant_locs[i].x,plant_locs[i].y,-planRotation);
		HRotate( temp_h, plant_locs[i].x, plant_locs[i].y, planRotation );
		HRotate( temp_h, plant_locs[i].x, plant_locs[i].y, plantRoatation );
{		Htransferrecs(key_plant,temp_h,FALSE);}

gFence_h := CreateCustomObject('Site Modifiers',0,0,0.00);
IF (gFencePolys[i] <> NIL) THEN temp_b := SetCustomObjectPath(gFence_h,gFencePolys[i]);
setrfield(gFence_h,'Site Modifiers','Config','Fence'); {NEW 3/9/04 -- last-minute fix -- RFA}
{ if we are in a 3D view then show the 3D fence polygon. }
IF is3DView THEN SetRField( gFence_h, 'Site Modifiers', 'Show 3D', 'True' );

				{ create stake objects. }
				stakeHandle := CreateCustomObject(kStakeObj, 0, 0, 0);
				IF (stakeHandle <> NIL) THEN BEGIN
					Move3DObj(stakeHandle, x, y, z);
					IF (inColID = 1) THEN WriteID(stakeHandle, textColumns[1]);
{					SetRField(stakeHandle, kStakeObj, kStyleField, kDefaultStyle);
```
```python
import vs

# Creates a custom object instance at the specified location and angle of
# rotation.
objectName = 'Example'
p = (0, 0)
rotationAngle = 45.0

objHandle = vs.CreateCustomObject(objectName, p, rotationAngle)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[CreateCustomObjectPath](CreateCustomObjectPath.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
