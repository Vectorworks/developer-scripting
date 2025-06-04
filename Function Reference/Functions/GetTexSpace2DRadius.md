# GetTexSpace2DRadius

## Description
Function GetTexSpace2DRadius returns the radius of the referenced texture space for applicable mapping types.

```pascal
FUNCTION GetTexSpace2DRadius(textureSpace : HANDLE): REAL;
```

```python
def vs.GetTexSpace2DRadius(textureSpace):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|

## Remarks
[[User:CBM-c-|_c_]] (2018 Dec. 29) Use [[VS:GetTexMapRealN]] instead. 


For applicable mapping types, gets the radius of the texture space.

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
