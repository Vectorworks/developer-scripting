# GetTexSpaceStartCap

## Description
Function GetTexSpaceStartCap returns whether the start cap of an extrude or sweep is textured.

```pascal
FUNCTION GetTexSpaceStartCap(textureSpace : HANDLE): BOOLEAN;
```

```python
def vs.GetTexSpaceStartCap(textureSpace):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|

## Remarks
Returns whether start cap of extrude or sweep is textured

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
resultOK := GetTexSpaceStartCap(textureSpace);
```
```python
import vs

# Function GetTexSpaceStartCap returns whether the start cap of an extrude or
# sweep is textured.
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetTexSpaceStartCap(textureSpace)
if ok:
    vs.Message('GetTexSpaceStartCap succeeded')
else:
    vs.Message('GetTexSpaceStartCap failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
