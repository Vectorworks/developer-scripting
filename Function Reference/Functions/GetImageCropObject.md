# GetImageCropObject

## Description
Get the crop of a cropped image.

```pascal
FUNCTION GetImageCropObject(obj : HANDLE): HANDLE;
```

```python
def vs.GetImageCropObject(obj):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |

## Examples
```pascal
resultH := GetImageCropObject(obj);
```
```python
import vs

# Get the crop of a cropped image.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetImageCropObject(obj)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
