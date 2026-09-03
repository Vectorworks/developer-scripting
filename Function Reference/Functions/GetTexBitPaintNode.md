# GetTexBitPaintNode

## Description
Function GetTexBitPaintNode returns the paint node of the referenced texture bitmap.

```pascal
FUNCTION GetTexBitPaintNode(textureBitmap : HANDLE): HANDLE;
```

```python
def vs.GetTexBitPaintNode(textureBitmap):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|

## Remarks
Returns the paint node that contains the texture bitmap's image bits

## Examples
```pascal
resultH := GetTexBitPaintNode(textureBitmap);
```
```python
import vs

# Function GetTexBitPaintNode returns the paint node of the referenced
# texture bitmap.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetTexBitPaintNode(textureBitmap)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
GetTexBitPaintNode is obsolete as of VectorWorks12.0<P>

Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
