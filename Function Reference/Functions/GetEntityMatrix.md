# GetEntityMatrix

## Description
Gets the matrix of the plane for a planar object.

```pascal
FUNCTION GetEntityMatrix(
				VAR objectHandle   : HANDLE;
				VAR offsetX        : REAL;
				VAR offsetY        : REAL;
				VAR offsetZ        : REAL;
				VAR rotationXAngle : REAL;
				VAR rotationYAngle : REAL;
				VAR rotationZAngle : REAL): BOOLEAN;
```

```python
def vs.GetEntityMatrix(objectHandle):
    return (BOOLEAN, offset, rotationXAngle, rotationYAngle, rotationZAngle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object for which the matrix of its plane is being obtained.|
|offsetX|REAL|The offset of the plane in current document units.|
|offsetY|REAL|The offset of the plane in current document units.|
|offsetZ|REAL|The offset of the plane in current document units.|
|rotationXAngle|REAL|The rotation of the plane about the X-axis in degrees.|
|rotationYAngle|REAL|The rotation of the plane about the Y-axis in degrees.|
|rotationZAngle|REAL|The rotation of the plane about the Z-axis in degrees.|

## Examples
```pascal
BEGIN
		bsb := GetEntityMatrix(parmHand, matX1, matY1, matZ1, matAngleX, matAngleY, matAngleZ);

{Fix for Slab objects in 3D non-horizontal plane}
isOK := GetEntityMatrix(pathH, matX1, matY1, matZ1, matAngleX, matAngleY, matAngleZ);
IF ((matAngleX <> 0) OR (matAngleY <> 0)) THEN BEGIN
	SetObjectVariableInt(gPluginObjH, 803, 1);{803 == ovCustomObjectSymType, 1 == k3DSym}
	SetPlanarRef(gPluginObjH, planarRef);
	isOK := SetEntityMatrix(gPluginObjH, matX1, matY1, matZ1, matAngleX, matAngleY, matAngleZ);

BEGIN
	result := GetEntityMatrix(objectHand, matX1,matY1,matZ1,matAngleX,matAngleY,matAngleZ);
	layerH := GetLayer( objectHand );
	GetLayerElevation( layerH, layerElevation, layerThickness );
```
```python
import vs

# Gets the matrix of the plane for a planar object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, offset, rotationXAngle, rotationYAngle, rotationZAngle = vs.GetEntityMatrix(objectHandle)
vs.Message('GetEntityMatrix returned: ' + str((ok, offset, rotationXAngle, rotationYAngle, rotationZAngle)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
