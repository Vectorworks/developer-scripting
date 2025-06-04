# AttachDefaultTextureSpace

## Description
Procedure AttachDefaultTextureSpace deletes any pre-existing space attached to the referenced object and creates a new one with the default object texture.

```pascal
PROCEDURE AttachDefaultTextureSpace(
				obj    : HANDLE;
				partID : INTEGER);
```

```python
def vs.AttachDefaultTextureSpace(obj, partID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Part ID (pass 1 for non-supporting objects).|

## Remarks
Deletes any pre-existing space attached to the object (with the specified part ID), creates a new one with the default value for this type of object, and attaches the texture space to the object.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
