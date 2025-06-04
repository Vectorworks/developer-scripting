# DeleteTextureSpace

## Description
Function DeleteTextureSpace deletes the texture space attached to the referenced object or object part.

```pascal
PROCEDURE DeleteTextureSpace(
				obj    : HANDLE;
				partID : INTEGER);
```

```python
def vs.DeleteTextureSpace(obj, partID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Part ID (pass 1 for non-supporting objects).|

## Remarks
Removes the texture space from this object.  To render textures correctly, an object must have both a non-zero texture ref and a texture space attached.  The reverse of this means that the texture ref for the object should be set to zero when this function is called.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
