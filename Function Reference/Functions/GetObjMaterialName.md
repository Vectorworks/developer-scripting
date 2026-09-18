# GetObjMaterialName

```pascal
FUNCTION GetObjMaterialName(
				h                : HANDLE;
				VAR materialName : STRING): BOOLEAN;
```

```python
def vs.GetObjMaterialName(h):
    return (BOOLEAN, materialName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|materialName|STRING|   |

## Examples
```pascal
resultOK := GetObjMaterialName(h, 'Example');
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, materialName = vs.GetObjMaterialName(h)
vs.Message('GetObjMaterialName returned: ' + str((ok, materialName)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
