# DBeam_GetObjAtFocus

## Description
Return the most recently created beam object

```pascal
FUNCTION DBeam_GetObjAtFocus : HANDLE;
```

```python
def vs.DBeam_GetObjAtFocus():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_GetObjAtFocus;
```
```python
import vs

# Return the most recently created beam object.
objHandle = vs.DBeam_GetObjAtFocus()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
