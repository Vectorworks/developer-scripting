# DBeam_GetLines

## Description
Return the most recently created beam object

```pascal
FUNCTION DBeam_GetLines : HANDLE;
```

```python
def vs.DBeam_GetLines():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_GetLines;
```
```python
import vs

# Return the most recently created beam object.
objHandle = vs.DBeam_GetLines()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
