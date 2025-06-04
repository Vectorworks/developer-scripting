# GetTextureShader

## Description
Function GetTextureShader returns the LightWorks internal property reference ID for the shader attached to the referenced texture.

```pascal
FUNCTION GetTextureShader(texture : HANDLE): LONGINT;
```

```python
def vs.GetTextureShader(texture):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|Handle to texture.|

## Remarks
Returns LightWorks internal property ref for the shader attached to this texture.

## Version
GetTextureShader is obsolete as of VectorWorks9.0<P>


Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
