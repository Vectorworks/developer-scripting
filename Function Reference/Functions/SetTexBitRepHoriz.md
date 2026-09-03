# SetTexBitRepHoriz

## Description
Procedure SetTexBitRepHoriz  sets the horizontal repeat flag for the referenced texture bitmap.

```pascal
PROCEDURE SetTexBitRepHoriz(
				textureBitmap : HANDLE;
				repeatHoriz   : BOOLEAN);
```

```python
def vs.SetTexBitRepHoriz(textureBitmap, repeatHoriz):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|repeatHoriz|BOOLEAN|Horizontal tiling setting.|

## Remarks
Sets the texture bitmap attribute to specify that it should repeat horizontally.

## Examples
```pascal
BEGIN
textureBitmap := CreateTextureBitmapN(shaderRecord);
SetTexBitRepHoriz(textureBitmap, FALSE);
SetTexBitRepVert(textureBitmap, FALSE);
IF textureBitmap <> NIL THEN
	BEGIN
	SetName(TextureHand,TextureName);
```
```python
import vs

# Procedure SetTexBitRepHoriz sets the horizontal repeat flag for the
# referenced texture bitmap.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer
repeatHoriz = True

vs.SetTexBitRepHoriz(textureBitmap, repeatHoriz)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
