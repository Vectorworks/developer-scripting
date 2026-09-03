# GetTextureSize

## Description
Returns the texture size in real-world inches.

```pascal
FUNCTION GetTextureSize(texture : HANDLE): REAL;
```

```python
def vs.GetTextureSize(texture):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|   |

## Examples
```pascal
resultVal := GetTextureSize(texture);
```
```python
import vs

# Returns the texture size in real-world inches.
texture = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetTextureSize(texture)
vs.Message('GetTextureSize returned: ' + str(value))
```

## Version
Availability: from VectorWorks10.1

## Category
* [Textures](../Categories/Textures.md)
