# SetImageCropVisible

## Description
Set the image crop visibility.

```pascal
PROCEDURE SetImageCropVisible(
				obj       : HANDLE;
				isVisible : BOOLEAN);
```

```python
def vs.SetImageCropVisible(obj, isVisible):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|isVisible|BOOLEAN|If TRUE the crop become visible, if FALSE - invisible.|

## Examples
```pascal
SetImageCropVisible(obj, TRUE);
```
```python
import vs

# Set the image crop visibility.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
isVisible = True

vs.SetImageCropVisible(obj, isVisible)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
