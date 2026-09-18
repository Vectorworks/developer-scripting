# DBeam_GetObjFallOff

## Description
Return the most recently created beam object

```pascal
FUNCTION DBeam_GetObjFallOff : HANDLE;
```

```python
def vs.DBeam_GetObjFallOff():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_GetObjFallOff;
```
```python
import vs

# Return the most recently created beam object.
objHandle = vs.DBeam_GetObjFallOff()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
