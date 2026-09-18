# SetMtlFillStyleByCls

```pascal
FUNCTION SetMtlFillStyleByCls(
				materialHandle : HANDLE;
				isByClass      : BOOLEAN): BOOLEAN;
```

```python
def vs.SetMtlFillStyleByCls(materialHandle, isByClass):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialHandle|HANDLE|   |
|isByClass|BOOLEAN|   |

## Examples
```pascal
resultOK := SetMtlFillStyleByCls(materialHandle, TRUE);
```
```python
import vs

materialHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
isByClass = True

ok = vs.SetMtlFillStyleByCls(materialHandle, isByClass)
if ok:
    vs.Message('SetMtlFillStyleByCls succeeded')
else:
    vs.Message('SetMtlFillStyleByCls failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
