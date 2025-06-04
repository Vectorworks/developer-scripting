# SetDefaultTextureSpace

## Description
Procedure SetDefaultTextureSpace sets the texture space for the referenced object to the VectorWorks object defaults.

```pascal
PROCEDURE SetDefaultTextureSpace(
				obj      : HANDLE;
				texSpace : HANDLE;
				partID   : INTEGER);
```

```python
def vs.SetDefaultTextureSpace(obj, texSpace, partID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|texSpace|HANDLE|Handle to texture space.|
|partID|INTEGER|Part ID (pass 1 for non-supporting objects).|

## Remarks
Sets texSpace to the default values for this type of object.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
