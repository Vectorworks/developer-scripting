# GetViewMatrix

## Description
Gets view matrix for layer or viewport object.

```pascal
FUNCTION GetViewMatrix(
				objectHandle                : HANDLE;
				VAR offsetX,offsetY,offsetZ : REAL;
				VAR rotationXAng            : REAL;
				VAR rotationYAng            : REAL;
				VAR rotationZAng            : REAL): BOOLEAN;
```

```python
def vs.GetViewMatrix(objectHandle):
    return (BOOLEAN, offset, rotationXAng, rotationYAng, rotationZAng)
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
gViewportInfo [gNumSheets2].View := viewToPopup (GetObjectVariableInt (h, 1007));
OK := GetViewMatrix (h, x, y, z, gViewportInfo [gNumSheets2].RotateX, gViewportInfo [gNumSheets2].RotateY, gViewportInfo [gNumSheets2].RotateZ);

boo := GetViewMatrix	(
						GetLayer(GetObject(RefGridPIOName)),
						VMatrixOffsetPt3D.x,
						VMatrixOffsetPt3D.y,
						VMatrixOffsetPt3D.z,
						VMatrixAngleX,
						VMatrixAngleY,
						VMatrixAngleZ
						);

{ get the rotation of the view if there is one }
currLayer := GetParent(objHand);
WHILE (currLayer <> NIL) & (GetType(currLayer) <> 31) DO currLayer := GetParent(currLayer);
boo := GetViewMatrix(currLayer, offsetX, offsetY, offsetZ, rotXAng, rotYAng, rotZAng);
boo := SetViewMatrix(currLayer, 0, 0, 0, 0, 0, 0);
```
```python
import vs

# Gets view matrix for layer or viewport object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, offset, rotationXAng, rotationYAng, rotationZAng = vs.GetViewMatrix(objectHandle)
vs.Message('GetViewMatrix returned: ' + str((ok, offset, rotationXAng, rotationYAng, rotationZAng)))
```

## Version
Availability: from VectorWorks10.5

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
