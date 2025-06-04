# GetTexSpaceOrientW

## Description
Procedure GetTexSpaceOrientW returns the vector that describes the w-axis of the referenced texture (from world space to texture space).

```pascal
PROCEDURE GetTexSpaceOrientW(
				textureSpace : HANDLE;
				VAR wXAxis   : REAL;
				VAR wYAxis   : REAL;
				VAR wZAxis   : REAL);
```

```python
def vs.GetTexSpaceOrientW(textureSpace):
    return (wXAxis, wYAxis, wZAxis)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|wXAxis|REAL|Returns w-axis vector X component.|
|wYAxis|REAL|Returns w-axis vector Y component.|
|wZAxis|REAL|Returns w-axis vector Z component.|

## Remarks
Returns the vector that describes the w-axis of the texture (from world space to texture space)

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
