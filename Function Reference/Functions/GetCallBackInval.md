# GetCallBackInval

## Description
Returns whether callbacks are invalidating portions of the screen that are being changed.

```pascal
FUNCTION GetCallBackInval : BOOLEAN;
```

```python
def vs.GetCallBackInval():
    return BOOLEAN
```

## Examples
```pascal
resultOK := GetCallBackInval;
```
```python
import vs

# Returns whether callbacks are invalidating portions of the screen that are
# being changed.
ok = vs.GetCallBackInval()
if ok:
    vs.Message('GetCallBackInval succeeded')
else:
    vs.Message('GetCallBackInval failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
