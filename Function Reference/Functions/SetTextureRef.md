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
See [[VS:GetTextureRef]].

From Pat Stanford on the VectorScript list: To set an object's texture to be "by class", it looks like you need to use SetTextureRef with a TextureRef of -1 to set an object to use the class texture. For multitextureable objects like walls, you will either have to use SetTextureRef multiple times to set each part to use the class texture, or you will need to Use SetObjExpandTexture with a variable of false to set all of the parts to the same setting prior to using the SetTextureRef.

From Peter Vandewalle: Setting wall textures "by class" by using a TextureRef of -1 as Pat Stanford indicated has to be applied to PartID 3 in version 2011: SetTextureRef (WallHandle, -1, 3);

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
