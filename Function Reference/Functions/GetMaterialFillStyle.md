# GetMaterialFillStyle

```pascal
FUNCTION GetMaterialFillStyle(materialHandle : HANDLE): LONGINT;
```

```python
def vs.GetMaterialFillStyle(materialHandle):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialHandle|HANDLE|   |

## Examples
```pascal
resultN := GetMaterialFillStyle(materialHandle);
```
```python
import vs

materialHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetMaterialFillStyle(materialHandle)
vs.Message('GetMaterialFillStyle returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
