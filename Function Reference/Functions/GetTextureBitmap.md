# GetTextureBitmap

## Description
Function GetTextureBitmap returns the bitmap object attached to the referenced texture.

```pascal
FUNCTION GetTextureBitmap(shaderRecord : HANDLE): HANDLE;
```

```python
def vs.GetTextureBitmap(shaderRecord):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|shaderRecord|HANDLE|Handle to shader record.|

## Remarks
Returns the bitmap object attached to the shader record, NIL if none

## Examples
```pascal
resultH := GetTextureBitmap(shaderRecord);
```
```python
import vs

# Function GetTextureBitmap returns the bitmap object attached to the
# referenced texture.
shaderRecord = vs.GetObject('MyRecord')  # handle to a record format

objHandle = vs.GetTextureBitmap(shaderRecord)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
