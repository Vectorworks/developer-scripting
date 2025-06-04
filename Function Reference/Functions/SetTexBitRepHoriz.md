# SetTexBitRepHoriz

## Description
Procedure SetTexBitRepHoriz  sets the horizontal repeat flag for the referenced texture bitmap.

```pascal
PROCEDURE SetTexBitRepHoriz(
				textureBitmap : HANDLE;
				repeatHoriz   : BOOLEAN);
```

```python
def vs.SetTexBitRepHoriz(textureBitmap, repeatHoriz):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|repeatHoriz|BOOLEAN|Horizontal tiling setting.|

## Remarks
Sets the texture bitmap attribute to specify that it should repeat horizontally.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
