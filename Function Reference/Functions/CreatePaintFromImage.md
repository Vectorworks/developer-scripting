# CreatePaintFromImage

## Description
Creates a paint node from an image resource.

```pascal
FUNCTION CreatePaintFromImage(image : HANDLE): HANDLE;
```

```python
def vs.CreatePaintFromImage(image):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|image|HANDLE|Handle to the image resource from which a paint node is to be created.|

## Examples
[ImageAndPaint](examples/ImageAndPaint.md)

```pascal
BEGIN
	TempPhotoRsrcHand := GetObject(TempPhotoRsrcName);
	TempPhotoObjHand := CreatePaintFromImage(TempPhotoRsrcHand);
```
```python
import vs

# Creates a paint node from an image resource.
image = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CreatePaintFromImage(image)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Textures](../Categories/Textures.md)
