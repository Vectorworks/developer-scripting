# CreateTextureBitmapD

## Description
This function takes a shader record and creates a Texture bitmap.

```pascal
FUNCTION CreateTextureBitmapD(parentShaderRecord : HANDLE): HANDLE;
```

```python
def vs.CreateTextureBitmapD(parentShaderRecord):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|parentShaderRecord|HANDLE|This is the shader record input that the texture bitmap will be attached to.|

## Examples
```pascal
resultH := CreateTextureBitmapD(parentShaderRecord);
```
```python
import vs

# This function takes a shader record and creates a Texture bitmap.
parentShaderRecord = vs.GetObject('MyRecord')  # handle to a record format

objHandle = vs.CreateTextureBitmapD(parentShaderRecord)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[SetTextureBitmap](SetTextureBitmap.md) 
| [CreateShaderRecord](CreateShaderRecord.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Textures](../Categories/Textures.md)
