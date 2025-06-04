# SetTexSpace2DRot

## Description
Procedure SetTexSpace2DRot sets the rotation of the referenced texture space.

```pascal
PROCEDURE SetTexSpace2DRot(
				textureSpace    : HANDLE;
				rotationDegrees : REAL);
```

```python
def vs.SetTexSpace2DRot(textureSpace, rotationDegrees):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|rotationDegrees|REAL|Rotation of texture space(in degrees).|

## Remarks
[[User:CBM-c-|_c_]], (2018.12.29) Don't use this: it works but will remove the mapping, tested on VW 2017, 2018. Use [[VS:GetTexMapRealN]] instead.


Sets rotation in degrees

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
