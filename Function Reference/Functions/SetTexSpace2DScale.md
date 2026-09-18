# SetTexSpace2DScale

## Description
Procedure SetTexSpace2DScale sets the 2D scale for the referenced texture space. Parameter scale specifies the new scale value.

```pascal
PROCEDURE SetTexSpace2DScale(
				textureSpace : HANDLE;
				scale        : REAL);
```

```python
def vs.SetTexSpace2DScale(textureSpace, scale):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|scale|REAL|Scale for texture space.|

## Remarks
Sets the 2D scale for this texture space as a multiple of a default size of 1.

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
	SetTexSpace2DRadius(temp2_h, JoistMapRadius);
END;
SetTexSpaceStartCap( temp2_h, JoistMapStartCap);
SetTexSpaceEndCap	( temp2_h, JoistMapEndCap);
SetTexSpace2DScale(temp2_h, JoistMapScale);
SetTexSpace2DOffset(temp2_h, JoistMapHorOffset, JoistMapVertOffset );
SetTexSpace2DRot(temp2_h , JoistMapRotation);

wallTextureScale := GetTexSpace2DScale( wallTextureSpace );
SetTexSpace2DScale( objTextureSpace, wallTextureScale );

SetTexSpace2DScale(hTextureSpace, Scaleim*VirtScrnWdth/GetObjectVariablereal(hTexture,511));
```
```python
import vs

# Procedure SetTexSpace2DScale sets the 2D scale for the referenced texture
# space.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
scale = 1.0

vs.SetTexSpace2DScale(textureSpace, scale)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
