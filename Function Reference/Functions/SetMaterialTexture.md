# SetMaterialTexture

```pascal
FUNCTION SetMaterialTexture(
				VAR materialHandle : HANDLE;
				textureIndex       : LONGINT): BOOLEAN;
```

```python
def vs.SetMaterialTexture(materialHandle, textureIndex):
    return (BOOLEAN, materialHandle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialHandle|HANDLE|   |
|textureIndex|LONGINT|   |

## Examples
```pascal
resultOK := SetMaterialTexture(materialHandle, 1);
```
```python
import vs

materialHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
textureIndex = 1

ok, materialHandle = vs.SetMaterialTexture(materialHandle, textureIndex)
vs.Message('SetMaterialTexture returned: ' + str((ok, materialHandle)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
