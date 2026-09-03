# GetTexBitmapOrigin

## Description
Procedure GetTexBitmapOrigin returns the origin of the bitmap applied to the referenced texture bitmap. The origin is measured in pixels, with the top left corner as (0,0).

```pascal
PROCEDURE GetTexBitmapOrigin(
				textureBitmap : HANDLE;
				VAR originX   : INTEGER;
				VAR originY   : INTEGER);
```

```python
def vs.GetTexBitmapOrigin(textureBitmap):
    return (originX, originY)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|originX|INTEGER|Returns X coordinate of bitmap origin.|
|originY|INTEGER|Returns Y coordinate of bitmap origin.|

## Remarks
Origin x and y are in pixels from paint node top left

## Examples
```pascal
GetTexBitmapOrigin(textureBitmap, 1, 2);
```
```python
import vs

# Procedure GetTexBitmapOrigin returns the origin of the bitmap applied to
# the referenced texture bitmap.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer

originX, originY = vs.GetTexBitmapOrigin(textureBitmap)
vs.Message('GetTexBitmapOrigin returned: ' + str((originX, originY)))
```

## Version
GetTexBitmapOrigin is obsolete as of VectorWorks9.0<P>

Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
