# SetTextureBitmap

## Description
Procedure SetTextureBitmap sets the bitmap object attached to the referenced texture. If no texture is desired then set textureBitmap to NIL.

```pascal
PROCEDURE SetTextureBitmap(
				shaderRecord  : HANDLE;
				textureBitmap : HANDLE);
```

```python
def vs.SetTextureBitmap(shaderRecord, textureBitmap):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|shaderRecord|HANDLE|Handle to shader record.|
|textureBitmap|HANDLE|Handle to texture bitmap.|

## Remarks
Sets the bitmap for a shader record, use NIL for no bitmap

## Examples
```pascal
SetTextureBitmap(shaderRecord, textureBitmap);
```
```python
import vs

# Procedure SetTextureBitmap sets the bitmap object attached to the
# referenced texture.
shaderRecord = vs.GetObject('MyRecord')  # handle to a record format
textureBitmap = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.SetTextureBitmap(shaderRecord, textureBitmap)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
