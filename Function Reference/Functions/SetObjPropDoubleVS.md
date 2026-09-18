# SetObjPropDoubleVS

## Description
?

```pascal
FUNCTION SetObjPropDoubleVS(
				PropertyID  : LONGINT;
				PropertyVal : REAL): BOOLEAN;
```

```python
def vs.SetObjPropDoubleVS(PropertyID, PropertyVal):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|PropertyID|LONGINT|   |
|PropertyVal|REAL|   |

## Examples
```pascal
resultOK := SetObjPropDoubleVS(1, 1.0);
```
```python
import vs

# ?.
PropertyID = 1
PropertyVal = 1.0

ok = vs.SetObjPropDoubleVS(PropertyID, PropertyVal)
if ok:
    vs.Message('SetObjPropDoubleVS succeeded')
else:
    vs.Message('SetObjPropDoubleVS failed')
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
