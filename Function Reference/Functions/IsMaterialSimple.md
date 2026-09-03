# IsMaterialSimple

```pascal
FUNCTION IsMaterialSimple(materialHandle : HANDLE): BOOLEAN;
```

```python
def vs.IsMaterialSimple(materialHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialHandle|HANDLE|   |

## Examples
```pascal
resultOK := IsMaterialSimple(materialHandle);
```
```python
import vs

materialHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsMaterialSimple(materialHandle)
if ok:
    vs.Message('IsMaterialSimple succeeded')
else:
    vs.Message('IsMaterialSimple failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
