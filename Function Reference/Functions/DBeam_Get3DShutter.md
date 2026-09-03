# DBeam_Get3DShutter

## Description
Return the created 3D shutter object

```pascal
FUNCTION DBeam_Get3DShutter : HANDLE;
```

```python
def vs.DBeam_Get3DShutter():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_Get3DShutter;
```
```python
import vs

# Return the created 3D shutter object.
objHandle = vs.DBeam_Get3DShutter()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
