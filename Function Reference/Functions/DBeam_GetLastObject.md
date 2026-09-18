# DBeam_GetLastObject

## Description
Return the most recently created beam object

```pascal
FUNCTION DBeam_GetLastObject : HANDLE;
```

```python
def vs.DBeam_GetLastObject():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_GetLastObject;
```
```python
import vs

# Return the most recently created beam object.
objHandle = vs.DBeam_GetLastObject()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
