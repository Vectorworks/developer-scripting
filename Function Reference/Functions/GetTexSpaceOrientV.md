# GetTexSpaceOrientV

## Description
Procedure GetTexSpaceOrientV returns the vector that describes the v-axis of the referenced texture (from world space to texture space).

```pascal
PROCEDURE GetTexSpaceOrientV(
				textureSpace : HANDLE;
				VAR vXAxis   : REAL;
				VAR vYAxis   : REAL;
				VAR vZAxis   : REAL);
```

```python
def vs.GetTexSpaceOrientV(textureSpace):
    return (vXAxis, vYAxis, vZAxis)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|vXAxis|REAL|Returns v-axis vector X component.|
|vYAxis|REAL|Returns v-axis vector Y component.|
|vZAxis|REAL|Returns v-axis vector Z component.|

## Remarks
Returns the vector that describes the v-axis of the texture (from world space to texture space)

## Examples
```pascal
GetTexSpaceOrientV( wallTextureSpace, xAxis, yAxis, zAxis );
SetTexSpaceOrientW( objTextureSpace, xAxis, yAxis, zAxis );
```
```python
import vs

# Procedure GetTexSpaceOrientV returns the vector that describes the v-axis
# of the referenced texture (from world space to texture space).
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer

vXAxis, vYAxis, vZAxis = vs.GetTexSpaceOrientV(textureSpace)
vs.Message('GetTexSpaceOrientV returned: ' + str((vXAxis, vYAxis, vZAxis)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
