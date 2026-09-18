# SetTexMapRealN

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector: offsetX:1, offsetY:2, scale2D:3, rotate2D:4, radius:5, matrix mat00 through mat32: 6-17

```pascal
PROCEDURE SetTexMapRealN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER;
				value      : REAL);
```

```python
def vs.SetTexMapRealN(obj, texPartID, texLayerID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|0 for base, >0 for decals|
|selector|INTEGER|   |
|value|REAL|   |

## Examples
```pascal
IF TextureIndex <> 0 THEN SetTextureRefN(LocObjHandle,TextureIndex,kTexturePartID,kTextureLayerID);
SetTexMapRealN (LocObjHandle,kTexturePartID,0,4,Deg2Rad(RotateTexture));

BEGIN
	RndImShft := (SentDiameter*(25.4/GetPrefReal(152)))/2;
	SetTexMapRealN (ObjHan,kTexturePartID,kTextureLayerID,3,(gDiagScale/100)*1.005*SentDiameter/GetObjectVariableReal(LocImageHandle,511));
	SetTexMapRealN (ObjHan,kTexturePartID,kTextureLayerID,1,(SentDiameter*(gDiagHoriz/100*(25.4/GetPrefReal(152)))-RndImShft));
	SetTexMapRealN (ObjHan,kTexturePartID,kTextureLayerID,2,(SentDiameter*(gDiagVert/100*(25.4/GetPrefReal(152)))));
END

SetTexMapRealN (h3D,kTexturePartID,kTextureLayerID,3,Scaleim*1.005*ActScreenWidth/GetObjectVariablereal(hTexture,511));
SetTexMapRealN (h3D,kTexturePartID,kTextureLayerID,2,(gScrnHt*moveimv));
```
```python
import vs

# Set map info for specific part of object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
texPartID = 1
texLayerID = 2
selector = 3
value = 1.0

vs.SetTexMapRealN(obj, texPartID, texLayerID, selector, value)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
