# SetTexSpaceEndCap

## Description
Procedure SetTexSpaceEndCap sets whether the end cap of a referenced extrude or sweep is textured.

```pascal
PROCEDURE SetTexSpaceEndCap(
				textureSpace   : HANDLE;
				endCapTextured : BOOLEAN);
```

```python
def vs.SetTexSpaceEndCap(textureSpace, endCapTextured):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|endCapTextured|BOOLEAN|Texture end cap status.|

## Remarks
Sets whether end cap of extrude or sweep is textured

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
