# SetDropShadowByCls

```pascal
PROCEDURE SetDropShadowByCls(
				h            : HANDLE;
				byClassValue : BOOLEAN);
```

```python
def vs.SetDropShadowByCls(h, byClassValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|byClassValue|BOOLEAN|   |

## Examples
```pascal
SetDropShadowByCls(h, TRUE);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer
byClassValue = True

vs.SetDropShadowByCls(h, byClassValue)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
