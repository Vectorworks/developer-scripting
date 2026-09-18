# Shift

## Description
Shift returns TRUE if the Shift key was depressed during the last user event. This function operates with the MouseDown, KeyDown, AutoKey, GetPt, GetPtL, GetLine, and GetRect calls.

```pascal
FUNCTION Shift : BOOLEAN;
```

```python
def vs.Shift():
    return BOOLEAN
```

## Examples
```pascal
resultOK := Shift;
```
```python
import vs

# Shift returns TRUE if the Shift key was depressed during the last user event.
ok = vs.Shift()
if ok:
    vs.Message('Shift succeeded')
else:
    vs.Message('Shift failed')
```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
