# LLayer

## Description
Function LLayer returns a handle to the last layer in a VectorWorks document.

```pascal
FUNCTION LLayer : HANDLE;
```

```python
def vs.LLayer():
    return HANDLE
```

## Examples
```pascal
resultH := LLayer;
```
```python
import vs

# Function LLayer returns a handle to the last layer in a VectorWorks document.
objHandle = vs.LLayer()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
