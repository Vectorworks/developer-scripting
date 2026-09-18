# SetTexBitRepVert

## Description
Procedure SetTexBitRepVert  sets the vertical repeat flag for the referenced texture bitmap. Parameter repeatVert toggles vertical tiling.

```pascal
PROCEDURE SetTexBitRepVert(
				textureBitmap : HANDLE;
				repeatVert    : BOOLEAN);
```

```python
def vs.SetTexBitRepVert(textureBitmap, repeatVert):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|repeatVert|BOOLEAN|Vertical tiling setting.|

## Remarks
Sets the texture bitmap attribute to specify that it should repeat vertically

## Examples
```pascal
BEGIN
textureBitmap := CreateTextureBitmapN(shaderRecord);
SetTexBitRepHoriz(textureBitmap, FALSE);
SetTexBitRepVert(textureBitmap, FALSE);
IF textureBitmap <> NIL THEN
	BEGIN
	SetName(TextureHand,TextureName);
	SetTextureSize(TextureHand, 2");
```
```python
import vs

# Procedure SetTexBitRepVert sets the vertical repeat flag for the referenced
# texture bitmap.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer
repeatVert = True

vs.SetTexBitRepVert(textureBitmap, repeatVert)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
