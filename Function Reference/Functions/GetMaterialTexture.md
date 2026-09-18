# GetMaterialTexture

```pascal
FUNCTION GetMaterialTexture(objectHandle : HANDLE): LONGINT;
```

```python
def vs.GetMaterialTexture(objectHandle):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|   |

## Examples
```pascal
BEGIN
	useMaterialArchComp := TRUE;
	IF (textureByMaterial) THEN
		archCompTextureID := GetMaterialTexture(archCompMaterialH);
END
```
```python
import vs

objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetMaterialTexture(objectHandle)
vs.Message('GetMaterialTexture returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
