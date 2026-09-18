# GetDropShadowByCls

```pascal
FUNCTION GetDropShadowByCls(H : HANDLE): BOOLEAN;
```

```python
def vs.GetDropShadowByCls(H):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|H|HANDLE|   |

## Examples
```pascal
resultOK := GetDropShadowByCls(H);
```
```python
import vs

H = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetDropShadowByCls(H)
if ok:
    vs.Message('GetDropShadowByCls succeeded')
else:
    vs.Message('GetDropShadowByCls failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
