# GetTexSpaceOrientU

## Description
Procedure GetTexSpaceOrientU returns the vector that describes the u-axis of the referenced texture (from world space to texture space).

```pascal
PROCEDURE GetTexSpaceOrientU(
				textureSpace : HANDLE;
				VAR uXAxis   : REAL;
				VAR uYAxis   : REAL;
				VAR uZAxis   : REAL);
```

```python
def vs.GetTexSpaceOrientU(textureSpace):
    return (uXAxis, uYAxis, uZAxis)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|uXAxis|REAL|Returns u-axis vector X component.|
|uYAxis|REAL|Returns u-axis vector Y component.|
|uZAxis|REAL|Returns u-axis vector Z component.|

## Remarks
Returns the vector that describes the u-axis of the texture (from world space to texture space)

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
