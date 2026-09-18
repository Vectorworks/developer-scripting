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

## Examples
```pascal
resultN := GetTextureShader(texture);
```
```python
import vs

# Function GetTextureShader returns the LightWorks internal property
# reference ID for the shader attached to the referenced texture.
texture = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetTextureShader(texture)
vs.Message('GetTextureShader returned: ' + str(resultN))
```

## Version
GetTextureShader is obsolete as of VectorWorks9.0<P>

Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
