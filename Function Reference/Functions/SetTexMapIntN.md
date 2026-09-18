# SetTexMapIntN

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector should be 1 to set the map type integer.

```pascal
PROCEDURE SetTexMapIntN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER;
				value      : INTEGER);
```

```python
def vs.SetTexMapIntN(obj, texPartID, texLayerID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|0 for base, >0 for decals|
|selector|INTEGER|   |
|value|INTEGER|   |

## Examples
```pascal
GetImageHandleIndex (gScrnImageIdx,gScrnImageFolder,GetRField(ghparm,kPIOName,'ScrnImage'),hTexture,gTextureRef);
SetDefaultTexMapN (h3D,kTexturePartID,kTextureLayerID);
SetTexturerefN(h3D,gTextureRef,kTexturePartID,kTextureLayerID);
IF (Str2Boo(GetRField(ghParm,kPIOName,'Curved'))) THEN
	SetTexMapIntN(h3D,kTexturePartID,kTextureLayerID,1,3);
SetTexMapBoolN (h3D,kTexturePartID,kTextureLayerID,1,TRUE);

IF (gCRTC) THEN
	SetTexMapIntN(h3D,kTexturePartID,kTextureLayerID,1,3);
```
```python
import vs

# Set map info for specific part of object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
texPartID = 1
texLayerID = 2
selector = 3
value = 10

vs.SetTexMapIntN(obj, texPartID, texLayerID, selector, value)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
