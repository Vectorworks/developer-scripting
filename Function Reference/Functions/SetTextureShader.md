# SetTextureShader

## Description
Procedure SetTextureShader sets the LightWorks internal property reference ID for the shader attached to the referenced texture.

```pascal
PROCEDURE SetTextureShader(
				texture     : HANDLE;
				shaderIndex : LONGINT);
```

```python
def vs.SetTextureShader(texture, shaderIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|Handle to texture.|
|shaderIndex|LONGINT|Shader ID value for texture.|

## Remarks
Sets the shader to a LightWorks internal property ref.

## Version
SetTextureShader is obsolete as of VectorWorks9.0<P>


Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
