# FActLayer

## Description
Function FActLayer returns a handle to the first object on the active layer. If the object does not exist, the function returns NIL.

```pascal
FUNCTION FActLayer : HANDLE;
```

```python
def vs.FActLayer():
    return HANDLE
```

## Examples
```pascal
resultH := FActLayer;
```
```python
import vs

# Function FActLayer returns a handle to the first object on the active layer.
objHandle = vs.FActLayer()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
