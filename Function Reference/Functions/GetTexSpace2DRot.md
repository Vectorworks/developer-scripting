# GetTexSpace2DRot

## Description
Function GetTexSpace2DRot returns the rotation of the referenced texture space (in degrees).

```pascal
FUNCTION GetTexSpace2DRot(textureSpace : HANDLE): REAL;
```

```python
def vs.GetTexSpace2DRot(textureSpace):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|

## Remarks
*\_c\_* (2018.12.29) Use [GetTexMapRealN](GetTexMapRealN.md) instead.

Returns rotation in degrees

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
tmpReal := GetTexSpace2DRot(wallTextureSpace);
```
```python
import vs

# Function GetTexSpace2DRot returns the rotation of the referenced texture
# space (in degrees).
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetTexSpace2DRot(textureSpace)
vs.Message('GetTexSpace2DRot returned: ' + str(value))
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
