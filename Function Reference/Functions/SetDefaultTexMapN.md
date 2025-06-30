# SetDefaultTexMapN

## Description
Set the object to have default texture mapping info. Texture resource being used is set with SetTextureRef. This routine replaces SetDefaultTexMap with version 2010 and above.

```pascal
PROCEDURE SetDefaultTexMapN(
				h          : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT);
```

```python
def vs.SetDefaultTexMapN(h, texPartID, texLayerID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The textured object|
|texPartID|LONGINT|The texture part ID|
|texLayerID|LONGINT|The texture layer ID, 0 for base, >0 for decals|

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
