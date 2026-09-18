# SetImageCropObject

## Description
By given image handle and crop handle, set the crop to the image.

```pascal
FUNCTION SetImageCropObject(
				image : HANDLE;
				crop  : HANDLE): BOOLEAN;
```

```python
def vs.SetImageCropObject(image, crop):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|image|HANDLE|   |
|crop|HANDLE|   |

## Examples
```pascal
resultOK := SetImageCropObject(image, crop);
```
```python
import vs

# By given image handle and crop handle, set the crop to the image.
image = vs.FSActLayer()  # handle to the first selected object on the active layer
crop = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.SetImageCropObject(image, crop)
if ok:
    vs.Message('SetImageCropObject succeeded')
else:
    vs.Message('SetImageCropObject failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
