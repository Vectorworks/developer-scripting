# SetTexBitPaintNode

## Description
Procedure SetTexBitPaintNode sets the paint node of the referenced texture bitmap.

```pascal
PROCEDURE SetTexBitPaintNode(
				textureBitmap : HANDLE;
				paintNode     : HANDLE);
```

```python
def vs.SetTexBitPaintNode(textureBitmap, paintNode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|paintNode|HANDLE|Paint node for texture bitmap.|

## Remarks
Sets the texture bitmap's image paint node

## Examples
```pascal
SetTexBitPaintNode(textureBitmap, paintNode);
```
```python
import vs

# Procedure SetTexBitPaintNode sets the paint node of the referenced texture
# bitmap.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer
paintNode = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.SetTexBitPaintNode(textureBitmap, paintNode)
```

## Version
SetTexBitPaintNode is obsolete as of VectorWorks12.0<P>

Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
