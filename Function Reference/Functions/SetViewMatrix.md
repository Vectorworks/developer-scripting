# SetViewMatrix

## Description
Sets view matrix for layer or viewport object.

```pascal
FUNCTION SetViewMatrix(
				objectHandle            : HANDLE;
				offsetX,offsetY,offsetZ : REAL;
				rotationXAng            : REAL;
				rotationYAng            : REAL;
				rotationZAng            : REAL): BOOLEAN;
```

```python
def vs.SetViewMatrix(objectHandle, offset, rotationXAng, rotationYAng, rotationZAng):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|   |
|offset|REAL|   |
|rotationXAng|REAL|   |
|rotationYAng|REAL|   |
|rotationZAng|REAL|   |

## Examples
```pascal
{view}
SetObjectVariableInt (viewportH, 1007, popupToView (gViewPortInfo [sheetNum].View));
IF popupToView (gViewPortInfo [sheetNum].View) = 0 THEN
	OK := SetViewMatrix (viewportH, 0, 0, 0, gViewPortInfo [sheetNum].RotateX, gViewPortInfo [sheetNum].RotateY, gViewPortInfo [sheetNum].RotateZ);

		'VMatrixAngleY			', VMatrixAngleY, Chr(13),
		'VMatrixAngleZ			', VMatrixAngleZ
		);
}
boo := SetViewMatrix	(
						pioParentVPHand,
						VMatrixOffsetPt3D.x,
						VMatrixOffsetPt3D.y,
						VMatrixOffsetPt3D.z,
						VMatrixAngleX,
						VMatrixAngleY,
						VMatrixAngleZ

{ get the rotation of the view if there is one }
currLayer := GetParent(objHand);
WHILE (currLayer <> NIL) & (GetType(currLayer) <> 31) DO currLayer := GetParent(currLayer);
boo := GetViewMatrix(currLayer, offsetX, offsetY, offsetZ, rotXAng, rotYAng, rotZAng);
boo := SetViewMatrix(currLayer, 0, 0, 0, 0, 0, 0);
```
```python
import vs

# Sets view matrix for layer or viewport object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
offset = 0.0
rotationXAng = 1.0
rotationYAng = 2.0
rotationZAng = 0.5

ok = vs.SetViewMatrix(objectHandle, offset, rotationXAng, rotationYAng, rotationZAng)
if ok:
    vs.Message('SetViewMatrix succeeded')
else:
    vs.Message('SetViewMatrix failed')
```

## Version
Availability: from VectorWorks10.5

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
