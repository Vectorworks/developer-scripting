# CreateRWBackground

## Description
Creates a Renderworks Background resource using the image from an existing Image resource. Width and height are set to default sizes relative to the page size.

```pascal
FUNCTION CreateRWBackground(imageResource : HANDLE): HANDLE;
```

```python
def vs.CreateRWBackground(imageResource):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|imageResource|HANDLE|   |

## Examples
```pascal
BEGIN
	pioRWBackRsrcHand := CreateRWBackground( pioPhotoRsrcHand );
	IF pioRWBackRsrcHand <> NIL THEN
	BEGIN
		SetName( pioRWBackRsrcHand, pioRWBackRsrcName );
		SetObjectVariableReal( pioRWBackRsrcHand, 1154, pPhotoPrintedWidth * pioLayScale * 25.4 / DocUPI );
```
```python
import vs

# Creates a Renderworks Background resource using the image from an existing
# Image resource.
imageResource = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CreateRWBackground(imageResource)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks14.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
