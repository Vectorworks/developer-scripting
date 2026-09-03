# Command

## Description
Command returns TRUE if the Command key (Mac) or Control key (Windows) was depressed during the last user event. This function operates with the MouseDown, KeyDown, AutoKey, GetPt, GetPtL, GetLine, and GetRect calls.

```pascal
FUNCTION Command : BOOLEAN;
```

```python
def vs.Command():
    return BOOLEAN
```

## Examples
```pascal
resultOK := Command;
```
```python
import vs

# Command returns TRUE if the Command key (Mac) or Control key (Windows) was
# depressed during the last user event.
ok = vs.Command()
if ok:
    vs.Message('Command succeeded')
else:
    vs.Message('Command failed')
```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
