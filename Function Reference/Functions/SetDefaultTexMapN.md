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

## Examples
```pascal
BEGIN
	TexIndex := Name2Index(MyTexName);
	SetDefaultTexMapN (ObjHan,kTexturePartID,kTextureLayerID);
	IF TexIndex <> 0 THEN SetTexturerefN(ObjHan,TexIndex, kTexturePartID,kTextureLayerID);
	SetTexMapBoolN (ObjHan,kTexturePartID,kTextureLayerID,1,TRUE);

ScaleIm := PSCALE/100;
MoveImH := PMOVEHOR/100*(25.4/GetPrefReal(152));
MoveImV := PMOVEVER/100*(25.4/GetPrefReal(152));
GetImageHandleIndex (gScrnImageIdx,gScrnImageFolder,GetRField(ghparm,kPIOName,'ScrnImage'),hTexture,gTextureRef);
SetDefaultTexMapN (h3D,kTexturePartID,kTextureLayerID);
SetTexturerefN(h3D,gTextureRef,kTexturePartID,kTextureLayerID);
IF (Str2Boo(GetRField(ghParm,kPIOName,'Curved'))) THEN
	SetTexMapIntN(h3D,kTexturePartID,kTextureLayerID,1,3);
SetTexMapBoolN (h3D,kTexturePartID,kTextureLayerID,1,TRUE);

SetDefaultTexMapN (hLEDPanel,kTexturePartID,kTextureLayerID);
SetTextureRefN(hLEDPanel,gTextureRef,kTexturePartID,kTextureLayerID);
SetTexMapBoolN (hLEDPanel,kTexturePartID,kTextureLayerID,1,TRUE);
```
```python
import vs

# Set the object to have default texture mapping info.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
texPartID = 1
texLayerID = 2

vs.SetDefaultTexMapN(h, texPartID, texLayerID)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
