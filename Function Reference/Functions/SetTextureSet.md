# SetTextureSet

## Description
Sets the texture set of an object.

```pascal
PROCEDURE SetTextureSet(
				obj        : HANDLE;
				textureSet : INTEGER);
```

```python
def vs.SetTextureSet(obj, textureSet):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|
|textureSet|INTEGER|The texture set. 0 - Object textures, 1 - Component textures|

## Examples
```pascal
SetTextureSet(obj, 1);
```
```python
import vs

# Sets the texture set of an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
textureSet = 1

vs.SetTextureSet(obj, textureSet)
```

## See Also
VS Functions:
[GetTextureSet](GetTextureSet.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Textures](../Categories/Textures.md)
