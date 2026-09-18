# IsDropShadowEnabled

```pascal
FUNCTION IsDropShadowEnabled(h : HANDLE): BOOLEAN;
```

```python
def vs.IsDropShadowEnabled(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
resultOK := IsDropShadowEnabled(h);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsDropShadowEnabled(h)
if ok:
    vs.Message('IsDropShadowEnabled succeeded')
else:
    vs.Message('IsDropShadowEnabled failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
