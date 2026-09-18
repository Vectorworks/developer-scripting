# SetTexSpace2DRadius

## Description
Procedure SetTexSpace2DRadius sets the radius of the referenced texture space for applicable mapping types.

```pascal
PROCEDURE SetTexSpace2DRadius(
				textureSpace : HANDLE;
				radius       : REAL);
```

```python
def vs.SetTexSpace2DRadius(textureSpace, radius):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|radius|REAL|Radius of texture space.|

## Remarks
For applicable mapping types, sets the radius of the texture space.

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
BEGIN
	SetTexSpaceKind(temp2_h, 1);
	SetTexSpace2DRadius(temp2_h, JoistMapRadius);
END;

tmpReal := GetTexSpace2DRadius( wallTextureSpace );
SetTexSpace2DRadius( objTextureSpace, tmpReal );
```
```python
import vs

# Procedure SetTexSpace2DRadius sets the radius of the referenced texture
# space for applicable mapping types.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
radius = 1.0

vs.SetTexSpace2DRadius(textureSpace, radius)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
