# CreateTextureBitmapN

## Description
Creates a texture bitmap object for the chosen shader record.  Brings up dialog to choose the image file.  Returns nil if user clicked Cancel or if the shader is not an image-based shader.

```pascal
FUNCTION CreateTextureBitmapN(shaderRecord : HANDLE): HANDLE;
```

```python
def vs.CreateTextureBitmapN(shaderRecord):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|shaderRecord|HANDLE|Handle to shader record.|

## Examples
```pascal
BEGIN
textureBitmap := CreateTextureBitmapN(shaderRecord);
SetTexBitRepHoriz(textureBitmap, FALSE);
SetTexBitRepVert(textureBitmap, FALSE);
IF textureBitmap <> NIL THEN
	BEGIN
```
```python
import vs

# Creates a texture bitmap object for the chosen shader record.
shaderRecord = vs.GetObject('MyRecord')  # handle to a record format

objHandle = vs.CreateTextureBitmapN(shaderRecord)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.1

## Category
* [Textures](../Categories/Textures.md)
