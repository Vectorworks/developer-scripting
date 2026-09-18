# SetTexMapBoolN

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector: init:1, flip:2, repH:3, repV:4, long edge:5, worldZ:6, auto align:7

```pascal
PROCEDURE SetTexMapBoolN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER;
				value      : BOOLEAN);
```

```python
def vs.SetTexMapBoolN(obj, texPartID, texLayerID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|   |
|selector|INTEGER|   |
|value|BOOLEAN|   |

## Examples
```pascal
BEGIN
	TexIndex := Name2Index(MyTexName);
	SetDefaultTexMapN (ObjHan,kTexturePartID,kTextureLayerID);
	IF TexIndex <> 0 THEN SetTexturerefN(ObjHan,TexIndex, kTexturePartID,kTextureLayerID);
	SetTexMapBoolN (ObjHan,kTexturePartID,kTextureLayerID,1,TRUE);

SetDefaultTexMapN (h3D,kTexturePartID,kTextureLayerID);
SetTexturerefN(h3D,gTextureRef,kTexturePartID,kTextureLayerID);
IF (Str2Boo(GetRField(ghParm,kPIOName,'Curved'))) THEN
	SetTexMapIntN(h3D,kTexturePartID,kTextureLayerID,1,3);
SetTexMapBoolN (h3D,kTexturePartID,kTextureLayerID,1,TRUE);

   SetTexMapBoolN (LEDMesh,kTexturePartID,kTextureLayerID,3,P__TileImage);
SetTexMapBoolN (LEDMesh,kTexturePartID,kTextureLayerID,4,P__TileImage);
```
```python
import vs

# Set map info for specific part of object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
texPartID = 1
texLayerID = 2
selector = 3
value = True

vs.SetTexMapBoolN(obj, texPartID, texLayerID, selector, value)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
