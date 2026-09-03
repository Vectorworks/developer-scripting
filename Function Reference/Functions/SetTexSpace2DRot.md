# SetTexSpace2DRot

## Description
Procedure SetTexSpace2DRot sets the rotation of the referenced texture space.

```pascal
PROCEDURE SetTexSpace2DRot(
				textureSpace    : HANDLE;
				rotationDegrees : REAL);
```

```python
def vs.SetTexSpace2DRot(textureSpace, rotationDegrees):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|rotationDegrees|REAL|Rotation of texture space(in degrees).|

## Remarks
\_c\_, (2018.12.29) Don't use this: it works but will remove the mapping, tested on VW 2017, 2018. Use [GetTexMapRealN](GetTexMapRealN.md) instead.

Sets rotation in degrees

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
BEGIN
	SetTexSpaceKind(TextSpaceHand,MapType);
	IF GetTypeN( H ) = 84 THEN
		SetTexSpace2DRot(TextSpaceHand, Deg2Rad(90));
END;

SetTexSpaceStartCap( temp2_h, JoistMapStartCap);
SetTexSpaceEndCap	( temp2_h, JoistMapEndCap);
SetTexSpace2DScale(temp2_h, JoistMapScale);
SetTexSpace2DOffset(temp2_h, JoistMapHorOffset, JoistMapVertOffset );
SetTexSpace2DRot(temp2_h , JoistMapRotation);

SetTexSpace2DRot( objTextureSpace, tmpReal );
```
```python
import vs

# Procedure SetTexSpace2DRot sets the rotation of the referenced texture space.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
rotationDegrees = 1.0

vs.SetTexSpace2DRot(textureSpace, rotationDegrees)
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
