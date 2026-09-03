# SetTexSpaceKind

## Description
Procedure SetTexSpaceKind sets the object type for referenced texture mapping space.

* Table - Texture Mapping Spaces

| Date Style | Constant |
|------------|----------|
| Plane | 0 |
| Sphere | 1 |
| Cylinder | 2 |
| Algorithmic | 3 |

```pascal
PROCEDURE SetTexSpaceKind(
				textureSpace : HANDLE;
				kind         : INTEGER);
```

```python
def vs.SetTexSpaceKind(textureSpace, kind):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|kind|INTEGER|Texture mapping space type.|

## Remarks
Sets the kind for the texture mapping space; 0 = Plane space, 1 = Sphere, 2 = Cylinder, and 3 = Algorithmic (Perimeter or Roof)

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
BEGIN
	SetTexSpaceKind(TextSpaceHand,MapType);
	IF GetTypeN( H ) = 84 THEN
		SetTexSpace2DRot(TextSpaceHand, Deg2Rad(90));
END;

SetTextureRef(temp_h, tempTextIndex , 0);
AttachDefaultTextureSpace(temp_h, 0);
temp2_h := GetTextureSpace(temp_h, 0);
IF JoistMapType = 'Plane' THEN SetTexSpaceKind(temp2_h, 0);
IF JoistMapType = 'Sphere' THEN
BEGIN
	SetTexSpaceKind(temp2_h, 1);
	SetTexSpace2DRadius(temp2_h, JoistMapRadius);

tmpInt := GetTexSpaceKind( wallTextureSpace );
SetTexSpaceKind( objTextureSpace, tmpInt);
```
```python
import vs

# Procedure SetTexSpaceKind sets the object type for referenced texture
# mapping space.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
kind = 0

vs.SetTexSpaceKind(textureSpace, kind)
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
