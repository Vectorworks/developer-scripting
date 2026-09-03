# DBeam_Get2DLines

## Description
Return the most recently created beam object

```pascal
FUNCTION DBeam_Get2DLines : HANDLE;
```

```python
def vs.DBeam_Get2DLines():
    return HANDLE
```

## Examples
```pascal
resultH := DBeam_Get2DLines;
```
```python
import vs

# Return the most recently created beam object.
objHandle = vs.DBeam_Get2DLines()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
