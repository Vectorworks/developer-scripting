# SetTexSpaceOrigin

## Description
Procedure SetTexSpaceOrigin sets the offset of the referenced texture space that takes coordinates from world space to texture space.

```pascal
PROCEDURE SetTexSpaceOrigin(
				textureSpace            : HANDLE;
				offsetX,offsetY,offsetZ : REAL);
```

```python
def vs.SetTexSpaceOrigin(textureSpace, offset):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|offset|REAL|Texture space offset value.|

## Remarks
Sets the offset that takes coordinates from world space to texture space

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
