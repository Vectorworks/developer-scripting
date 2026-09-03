# CreatePaintFromImgN

## Description
Creates a paint node from an image resource on the specified location and rotation.

```pascal
FUNCTION CreatePaintFromImgN(
				image  : HANDLE;
				locPt  : REAL;
				rotDeg : REAL): HANDLE;
```

```python
def vs.CreatePaintFromImgN(image, locPt, rotDeg):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|image|HANDLE|Handle to the image resource from which a paint node is to be created.|
|locPt|REAL|Location of the new paint node.|
|rotDeg|REAL|Rotation of the paint node in degrees.|

## Remarks
[[User:Orso.b.schmid|Orso]] [2012.11.27]: A Bitmap (paint) object is created on drawing.

## Examples
```pascal
pioPhotoObjHand := CreatePaintFromImgN( pioPhotoRsrcHand, 0, 0, 0 );
pioPhotoRsrcWidth := HWidth( pioPhotoObjHand );
pioPhotoRsrcHeight := HHeight( pioPhotoObjHand );
pioPhotoRsrcPixelW := GetObjectVariableLongint( pioPhotoObjHand, 530 );
pioPhotoRsrcPixelH := GetObjectVariableLongint( pioPhotoObjHand, 531 );
```
```python
import vs

# Creates a paint node from an image resource on the specified location and
# rotation.
image = vs.FSActLayer()  # handle to the first selected object on the active layer
locPt = 1.0
rotDeg = 2.0

objHandle = vs.CreatePaintFromImgN(image, locPt, rotDeg)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Textures](../Categories/Textures.md)
