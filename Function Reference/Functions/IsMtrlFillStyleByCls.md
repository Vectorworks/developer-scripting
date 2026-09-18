# IsMtrlFillStyleByCls

```pascal
FUNCTION IsMtrlFillStyleByCls(materialHandle : HANDLE): BOOLEAN;
```

```python
def vs.IsMtrlFillStyleByCls(materialHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialHandle:|HANDLE|   |

## Examples
```pascal
resultOK := IsMtrlFillStyleByCls(materialHandle);
```
```python
import vs

materialHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsMtrlFillStyleByCls(materialHandle)
if ok:
    vs.Message('IsMtrlFillStyleByCls succeeded')
else:
    vs.Message('IsMtrlFillStyleByCls failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
