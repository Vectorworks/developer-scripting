# SetTexSpaceStartCap

## Description
Procedure SetTexSpaceStartCap sets the texture status of a referenced sweep or extrude.

```pascal
PROCEDURE SetTexSpaceStartCap(
				textureSpace     : HANDLE;
				startCapTextured : BOOLEAN);
```

```python
def vs.SetTexSpaceStartCap(textureSpace, startCapTextured):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|startCapTextured|BOOLEAN|Texture start cap status.|

## Remarks
Sets whether start cap of extrude or sweep is textured

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
BEGIN
	SetTexSpaceKind(temp2_h, 2);
	SetTexSpace2DRadius(temp2_h, JoistMapRadius);
END;
SetTexSpaceStartCap( temp2_h, JoistMapStartCap);
SetTexSpaceEndCap	( temp2_h, JoistMapEndCap);
SetTexSpace2DScale(temp2_h, JoistMapScale);
SetTexSpace2DOffset(temp2_h, JoistMapHorOffset, JoistMapVertOffset );
SetTexSpace2DRot(temp2_h , JoistMapRotation);
```
```python
import vs

# Procedure SetTexSpaceStartCap sets the texture status of a referenced sweep
# or extrude.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
startCapTextured = True

vs.SetTexSpaceStartCap(textureSpace, startCapTextured)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
