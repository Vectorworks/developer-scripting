# SetTexBitmapOrigin

## Description
Procedure SetTexBitmapOrigin sets the origin of the bitmap applied to the referenced texture bitmap. The origin is measured in pixels, with the top left corner as (0,0).

```pascal
PROCEDURE SetTexBitmapOrigin(
				textureBitmap : HANDLE;
				originX       : INTEGER;
				originY       : INTEGER);
```

```python
def vs.SetTexBitmapOrigin(textureBitmap, originX, originY):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|originX|INTEGER|X coordinate of bitmap origin.|
|originY|INTEGER|Y coordinate of bitmap origin.|

## Remarks
Origin x and y are in pixels from paint node top left

## Version
SetTexBitmapOrigin is obsolete as of VectorWorks9.0<P>


Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
