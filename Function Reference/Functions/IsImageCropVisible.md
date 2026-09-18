# IsImageCropVisible

## Description
Check is the crop of the image visible.

```pascal
FUNCTION IsImageCropVisible(obj : HANDLE): BOOLEAN;
```

```python
def vs.IsImageCropVisible(obj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |

## Examples
```pascal
resultOK := IsImageCropVisible(obj);
```
```python
import vs

# Check is the crop of the image visible.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsImageCropVisible(obj)
if ok:
    vs.Message('IsImageCropVisible succeeded')
else:
    vs.Message('IsImageCropVisible failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
