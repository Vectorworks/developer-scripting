# CreateTextureBitmap

## Description
Function CreateTextureBitmap creates a new default texture bitmap in a VectorWorks document.

```pascal
FUNCTION CreateTextureBitmap : HANDLE;
```

```python
def vs.CreateTextureBitmap():
    return HANDLE
```

## Remarks
Creates a new default texture bitmap, with no paint node attached.  Texture bitmap's paint node should be attached before this texture bitmap is used by MiniCAD ([SetTexBitPaintNode](SetTexBitPaintNode.md)).

## See Also
VS Functions:
[CreateTextureBitmapN](CreateTextureBitmapN.md)

## Version
CreateTextureBitmap is obsolete as of VectorWorks 10.1


Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
