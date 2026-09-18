# CLDropShadowEnabled

```pascal
FUNCTION CLDropShadowEnabled(className : STRING): BOOLEAN;
```

```python
def vs.CLDropShadowEnabled(className):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|   |

## Examples
```pascal
resultOK := CLDropShadowEnabled('Wall');
```
```python
import vs

className = 'None'

ok = vs.CLDropShadowEnabled(className)
if ok:
    vs.Message('CLDropShadowEnabled succeeded')
else:
    vs.Message('CLDropShadowEnabled failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Classes](../Categories/Classes.md)
