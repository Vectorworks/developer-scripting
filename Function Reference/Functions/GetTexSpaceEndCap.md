# GetTexSpaceEndCap

## Description
Function GetTexSpaceEndCap returns whether the end cap of the referenced extrude or sweep is textured.

```pascal
FUNCTION GetTexSpaceEndCap(textureSpace : HANDLE): BOOLEAN;
```

```python
def vs.GetTexSpaceEndCap(textureSpace):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|

## Remarks
Returns whether end cap of extrude or sweep is textured

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
