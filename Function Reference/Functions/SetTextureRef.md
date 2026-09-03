# SetTextureRef

## Description
Function SetTextureRef sets the texture reference ID for the referenced object.

```pascal
PROCEDURE SetTextureRef(
				obj        : HANDLE;
				textureRef : LONGINT;
				partID     : INTEGER);
```

```python
def vs.SetTextureRef(obj, textureRef, partID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|textureRef|LONGINT|Texture reference ID.|
|partID|INTEGER|Part to be assigned texture reference.|

## Remarks
See [GetTextureRef](GetTextureRef.md).

From Pat Stanford on the VectorScript list: To set an object's texture to be "by class", it looks like you need to use SetTextureRef with a TextureRef of -1 to set an object to use the class texture. For multitextureable objects like walls, you will either have to use SetTextureRef multiple times to set each part to use the class texture, or you will need to Use SetObjExpandTexture with a variable of false to set all of the parts to the same setting prior to using the SetTextureRef.

From Peter Vandewalle: Setting wall textures "by class" by using a TextureRef of -1 as Pat Stanford indicated has to be applied to PartID 3 in version 2011: SetTextureRef (WallHandle, -1, 3);

## Examples
```pascal
BEGIN
TextureIDX := GetClTextureG(pHidden);
IF TextureIDX <> 0 THEN
	 SetTextureRef(parmHand,TextureIDX,0);
END;

Wall(-(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi));
SetObjExpandTexture(lNewObj,FALSE);
SetTextureRef(lNewObj,-1,7);
WallCap(FALSE,FALSE,FALSE,-3*upi,3*upi);
WallCap(TRUE,FALSE,FALSE,3*upi,-3*upi);
result := SetWallOverallHeights(lnewobj,0,0,'',cHeight,0,0,'',cHeight);
WallPeak((cWidth/2-3*upi),cRise+cHeight);

BEGIN
	SetTextureRef (objectH, -1, 0);
	SetTextureRef (objectH, -1, 1);
	SetTextureRef (objectH, -1, 2);
END ELSE
BEGIN
```
```python
import vs

# Function SetTextureRef sets the texture reference ID for the referenced object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
textureRef = 1
partID = 2

vs.SetTextureRef(obj, textureRef, partID)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
