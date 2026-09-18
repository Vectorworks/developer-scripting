# SetTexSpaceEndCap

## Description
Procedure SetTexSpaceEndCap sets whether the end cap of a referenced extrude or sweep is textured.

```pascal
PROCEDURE SetTexSpaceEndCap(
				textureSpace   : HANDLE;
				endCapTextured : BOOLEAN);
```

```python
def vs.SetTexSpaceEndCap(textureSpace, endCapTextured):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|endCapTextured|BOOLEAN|Texture end cap status.|

## Remarks
Sets whether end cap of extrude or sweep is textured

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
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

# Procedure SetTexSpaceEndCap sets whether the end cap of a referenced
# extrude or sweep is textured.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
endCapTextured = True

vs.SetTexSpaceEndCap(textureSpace, endCapTextured)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
