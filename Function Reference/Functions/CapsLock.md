# CapsLock

## Description
CapsLock returns TRUE if the Caps Lock was depressed during the last user event. This function operates with the MouseDown, KeyDown, AutoKey, GetPt, GetPtL, GetLine, and GetRect calls.

```pascal
FUNCTION CapsLock : BOOLEAN;
```

```python
def vs.CapsLock():
    return BOOLEAN
```

## Examples
```pascal
resultOK := CapsLock;
```
```python
import vs

# CapsLock returns TRUE if the Caps Lock was depressed during the last user
# event.
ok = vs.CapsLock()
if ok:
    vs.Message('CapsLock succeeded')
else:
    vs.Message('CapsLock failed')
```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
