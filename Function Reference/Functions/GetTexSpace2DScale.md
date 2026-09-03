# GetTexSpace2DScale

## Description
Function GetTexSpace2DScale returns the 2D scale for the referenced texture space.

```pascal
FUNCTION GetTexSpace2DScale(textureSpace : HANDLE): REAL;
```

```python
def vs.GetTexSpace2DScale(textureSpace):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|

## Remarks
*\_c\_* (2018 Dec. 29) Use [GetTexMapRealN](GetTexMapRealN.md) instead.

Gets the 2D scale for this texture space as a multiple of a default size of 1.

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
wallTextureScale := GetTexSpace2DScale( wallTextureSpace );
SetTexSpace2DScale( objTextureSpace, wallTextureScale );
```
```python
import vs

# Function GetTexSpace2DScale returns the 2D scale for the referenced texture
# space.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetTexSpace2DScale(textureSpace)
vs.Message('GetTexSpace2DScale returned: ' + str(value))
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
