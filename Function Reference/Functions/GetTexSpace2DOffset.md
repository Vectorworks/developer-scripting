# GetTexSpace2DOffset

## Description
Procedure GetTexSpace2DOffset returns the 2D offset for the referenced texture space in real-world inches.

```pascal
PROCEDURE GetTexSpace2DOffset(
				textureSpace : HANDLE;
				VAR offsetU  : REAL;
				VAR offsetV  : REAL);
```

```python
def vs.GetTexSpace2DOffset(textureSpace):
    return (offsetU, offsetV)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|offsetU|REAL|Returns texture offset U component.|
|offsetV|REAL|returns texture offset V component.|

## Remarks
*\_c\_*, (2018.12.29) Use [GetTexMapRealN](GetTexMapRealN.md) instead.


Gets the 2D offset for this texture space in real-world inches.

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
