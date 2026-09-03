# LDevice_GetActSym

## Description
Get the active Ligtning symbol form the resource content

```pascal
FUNCTION LDevice_GetActSym : HANDLE;
```

```python
def vs.LDevice_GetActSym():
    return HANDLE
```

## Examples
```pascal
resultH := LDevice_GetActSym;
```
```python
import vs

# Get the active Ligtning symbol form the resource content.
objHandle = vs.LDevice_GetActSym()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2019

## Category
* [Spotlight](../Categories/Spotlight.md)
