# CreateTexture

## Description
Function CreateTexture creates a new texture object with default values.

```pascal
FUNCTION CreateTexture : HANDLE;
```

```python
def vs.CreateTexture():
    return HANDLE
```

## Remarks
Creates a new texture object handle with default values

## Examples
```pascal
resultH := CreateTexture;
```
```python
import vs

# Function CreateTexture creates a new texture object with default values.
objHandle = vs.CreateTexture()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
