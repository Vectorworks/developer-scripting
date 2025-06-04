# SetTexSpaceOrientV

## Description
Procedure SetTexSpaceOrientV specifies the vector that describes the v-axis of the referenced texture (from world space to texture space).

```pascal
PROCEDURE SetTexSpaceOrientV(
				textureSpace : HANDLE;
				vXAxis       : REAL;
				vYAxis       : REAL;
				vZAxis       : REAL);
```

```python
def vs.SetTexSpaceOrientV(textureSpace, vXAxis, vYAxis, vZAxis):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|vXAxis|REAL|Sets v-axis vector X component.|
|vYAxis|REAL|Sets v-axis vector Y component.|
|vZAxis|REAL|Sets v-axis vector Z component.|

## Remarks
Sets the v-axis for the texture space (from world space to texture space)

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
