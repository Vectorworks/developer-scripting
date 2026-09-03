# IsImageCropped

## Description
Check is the given image cropped.

```pascal
FUNCTION IsImageCropped(obj : HANDLE): BOOLEAN;
```

```python
def vs.IsImageCropped(obj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |

## Examples
```pascal
resultOK := IsImageCropped(obj);
```
```python
import vs

# Check is the given image cropped.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsImageCropped(obj)
if ok:
    vs.Message('IsImageCropped succeeded')
else:
    vs.Message('IsImageCropped failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
