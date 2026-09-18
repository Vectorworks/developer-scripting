# DBeam_Get2DObjFOff

## Description
Return the most recently created beam object

```pascal
FUNCTION DBeam_Get2DObjFOff : HANDLE;
```

```python
def vs.DBeam_Get2DObjFOff():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_Get2DObjFOff;
```
```python
import vs

# Return the most recently created beam object.
objHandle = vs.DBeam_Get2DObjFOff()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
