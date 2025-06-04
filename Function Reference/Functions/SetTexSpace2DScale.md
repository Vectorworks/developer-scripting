# SetTexSpace2DScale

## Description
Procedure SetTexSpace2DScale sets the 2D scale for the referenced texture space. Parameter scale specifies the new scale value.

```pascal
PROCEDURE SetTexSpace2DScale(
				textureSpace : HANDLE;
				scale        : REAL);
```

```python
def vs.SetTexSpace2DScale(textureSpace, scale):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|scale|REAL|Scale for texture space.|

## Remarks
Sets the 2D scale for this texture space as a multiple of a default size of 1.

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
