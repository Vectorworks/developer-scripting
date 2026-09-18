# GetTextureSet

## Description
Gets the texture set of an object.

```pascal
FUNCTION GetTextureSet(obj : HANDLE): INTEGER;
```

```python
def vs.GetTextureSet(obj):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|

## Examples
```pascal
resultN := GetTextureSet(obj);
```
```python
import vs

# Gets the texture set of an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetTextureSet(obj)
vs.Message('GetTextureSet returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetTextureSet](SetTextureSet.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Textures](../Categories/Textures.md)
