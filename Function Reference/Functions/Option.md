# Option

## Description
Option return TRUE if the Option key (Mac) or Alt key (Windows) was depressed during the last user event. This function operates with the MouseDown, KeyDown, AutoKey, GetPt, GetPtL, GetLine, and GetRect calls.

```pascal
FUNCTION Option : BOOLEAN;
```

```python
def vs.Option():
    return BOOLEAN
```

## Examples
```pascal
resultOK := Option;
```
```python
import vs

# Option return TRUE if the Option key (Mac) or Alt key (Windows) was
# depressed during the last user event.
ok = vs.Option()
if ok:
    vs.Message('Option succeeded')
else:
    vs.Message('Option failed')
```

## See Also
VS Functions:
[MouseDown](MouseDown.md) 
| [KeyDown](KeyDown.md) 
| [AutoKey](AutoKey.md)

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
