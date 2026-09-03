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

## Examples
```pascal
		bsb := SetEntityMatrix(parmHand, matX1 , matY1,matZ1, matAngleX, matAngleY, matAngleZ);
		SetRField(parmHand, parmName,'PrevStyle', Concat(gCabStyleI));
END;

isOK := GetEntityMatrix(pathH, matX1, matY1, matZ1, matAngleX, matAngleY, matAngleZ);
IF ((matAngleX <> 0) OR (matAngleY <> 0)) THEN BEGIN
	SetObjectVariableInt(gPluginObjH, 803, 1);{803 == ovCustomObjectSymType, 1 == k3DSym}
	SetPlanarRef(gPluginObjH, planarRef);
	isOK := SetEntityMatrix(gPluginObjH, matX1, matY1, matZ1, matAngleX, matAngleY, matAngleZ);
END;

BEGIN
	FlipHybMatrixObj( parmHand, 0 );
	bsb := GetEntityMatrix( parmHand, offsetX, offsetY, offsetZ, rotXAngle, rotYAngle, rotZangle );
	bsb := SetEntityMatrix( parmHand, offsetX, offsetY, offsetZ, rotXAngle, rotYAngle, rotZangle+180);
END;
```
```python
import vs

# Sets the matrix of the plane for a planar object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
offset = 0.0
rotationXAngle = 45.0
rotationYAngle = 90.0
rotationZAngle = 30.0

ok = vs.SetEntityMatrix(objectHandle, offset, rotationXAngle, rotationYAngle, rotationZAngle)
if ok:
    vs.Message('SetEntityMatrix succeeded')
else:
    vs.Message('SetEntityMatrix failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
