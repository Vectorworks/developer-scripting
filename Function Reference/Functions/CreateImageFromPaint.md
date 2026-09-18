# CreateImageFromPaint

## Description
Creates an image resource from a paint node.

```pascal
FUNCTION CreateImageFromPaint(
				paint     : HANDLE;
				imageName : STRING): HANDLE;
```

```python
def vs.CreateImageFromPaint(paint, imageName):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paint|HANDLE|Handle to the paint node to be used to create the image resource.|
|imageName|STRING|User-specified name to be used to identify the newly created image resource.|

## Examples
[ImageAndPaint](examples/ImageAndPaint.md)

```pascal
resultH := CreateImageFromPaint(paint, 'Example');
```
```python
import vs

# Creates an image resource from a paint node.
paint = vs.FSActLayer()  # handle to the first selected object on the active layer
imageName = 'Example'

objHandle = vs.CreateImageFromPaint(paint, imageName)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
