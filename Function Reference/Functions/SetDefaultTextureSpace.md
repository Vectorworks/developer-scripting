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

## Examples
```pascal
SetDefaultTextureSpace(obj, texSpace, 1);
```
```python
import vs

# Procedure SetDefaultTextureSpace sets the texture space for the referenced
# object to the VectorWorks object defaults.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
texSpace = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
partID = 1

vs.SetDefaultTextureSpace(obj, texSpace, partID)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
