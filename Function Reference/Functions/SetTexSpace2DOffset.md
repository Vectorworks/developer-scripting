# SetTexSpace2DOffset

## Description
Procedure SetTexSpace2DOffset sets the 2D offset for the referenced texture space in real-world inches.

```pascal
PROCEDURE SetTexSpace2DOffset(
				textureSpace : HANDLE;
				offsetU      : REAL;
				offsetV      : REAL);
```

```python
def vs.SetTexSpace2DOffset(textureSpace, offsetU, offsetV):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|offsetU|REAL|Texture offset U component.|
|offsetV|REAL|Texture offset V component.|

## Remarks
Sets the 2D offset for this texture space in real-world inches.

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
END;
SetTexSpaceStartCap( temp2_h, JoistMapStartCap);
SetTexSpaceEndCap	( temp2_h, JoistMapEndCap);
SetTexSpace2DScale(temp2_h, JoistMapScale);
SetTexSpace2DOffset(temp2_h, JoistMapHorOffset, JoistMapVertOffset );
SetTexSpace2DRot(temp2_h , JoistMapRotation);

GetTexSpace2DOffset( wallTextureSpace, uOffset, vOffset );
SetTexSpace2DOffset( objTextureSpace, uOffset, vOffset );

SetTexSpace2DOffset(hTextureSpace, (VirtScrnWdth*moveimh)+ImageXShift, (VirtScrnHeight*moveimv)+ImageZShift);
```
```python
import vs

# Procedure SetTexSpace2DOffset sets the 2D offset for the referenced texture
# space in real-world inches.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
offsetU = 0.0
offsetV = 0.0

vs.SetTexSpace2DOffset(textureSpace, offsetU, offsetV)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
