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

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
