# GetTexSpaceOrigin

## Description
Procedure GetTexSpaceOrigin returns the offset of the referenced texture space that takes coordinates from world space to texture space.

```pascal
PROCEDURE GetTexSpaceOrigin(
				textureSpace                : HANDLE;
				VAR offsetX,offsetY,offsetZ : REAL);
```

```python
def vs.GetTexSpaceOrigin(textureSpace):
    return offset
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|offset|REAL|Returns texture space offset value.|

## Remarks
Returns the offset that takes coordinates from world space to texture space

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
Begin
	GetTexSpaceOrigin( wallTextureSpace, xOffset, yOffset, zOffset );
	xOffset := -xOffset;
	yOffset := -yOffset;
	zOffset := -zOffset;
```
```python
import vs

# Procedure GetTexSpaceOrigin returns the offset of the referenced texture
# space that takes coordinates from world space to texture space.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetTexSpaceOrigin(textureSpace)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
