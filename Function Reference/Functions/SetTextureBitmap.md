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

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
