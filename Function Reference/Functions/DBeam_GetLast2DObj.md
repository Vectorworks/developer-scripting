# DBeam_GetLast2DObj

## Description
Return the most recently created 2D beam object

```pascal
FUNCTION DBeam_GetLast2DObj : HANDLE;
```

```python
def vs.DBeam_GetLast2DObj():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_GetLast2DObj;
```
```python
import vs

# Return the most recently created 2D beam object.
objHandle = vs.DBeam_GetLast2DObj()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
