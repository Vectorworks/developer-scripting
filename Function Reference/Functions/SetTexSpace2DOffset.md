# SetTexSpace2DOffset

## Description
Procedure SetTexSpace2DOffset sets the 2D offset for the referenced texture space in real-world inches.

```pascal
PROCEDURE SetTexSpace2DOffset(
				textureSpace : HANDLE;
				offsetU      : REAL;
				offsetV      : REAL);
```

```python
def vs.SetTexSpace2DOffset(textureSpace, offsetU, offsetV):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|offsetU|REAL|Texture offset U component.|
|offsetV|REAL|Texture offset V component.|

## Remarks
Sets the 2D offset for this texture space in real-world inches.

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
