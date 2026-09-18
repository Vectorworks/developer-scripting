# DBeam_GetLines2FOff

## Description
Return the most recently created beam object

```pascal
FUNCTION DBeam_GetLines2FOff : HANDLE;
```

```python
def vs.DBeam_GetLines2FOff():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_GetLines2FOff;
```
```python
import vs

# Return the most recently created beam object.
objHandle = vs.DBeam_GetLines2FOff()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
