# GetShaderRecord

## Description
Returns the shader record of the specified family (1 = color, 2 = reflectivity, 3 = transparency, 4 = bump), if one is attached to the texture.

```pascal
FUNCTION GetShaderRecord(
				texture : HANDLE;
				family  : LONGINT): HANDLE;
```

```python
def vs.GetShaderRecord(texture, family):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|Get the shader record attached to this texture.|
|family|LONGINT|The kind of shader to retrieve (1 = color, 2 = reflectivity, 3 = transparency, 4 = bump).|

## Examples
```pascal
ShaderRecHndl := GetShaderRecord(LocImageHandle,2);
```
```python
import vs

# Returns the shader record of the specified family (1 = color, 2 =
# reflectivity, 3 = transparency, 4 = bump), if one is attached to the
# texture.
texture = vs.FSActLayer()  # handle to the first selected object on the active layer
family = 1

objHandle = vs.GetShaderRecord(texture, family)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.1

## Category
* [Textures](../Categories/Textures.md)
