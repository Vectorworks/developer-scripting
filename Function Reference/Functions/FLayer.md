# FLayer

## Description
Function FLayer returns a handle to the first layer in a VectorWorks document.

```pascal
FUNCTION FLayer : HANDLE;
```

```python
def vs.FLayer():
    return HANDLE
```

## Examples
```pascal
resultH := FLayer;
```
```python
import vs

# Function FLayer returns a handle to the first layer in a VectorWorks document.
objHandle = vs.FLayer()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```
See also in tutorials: [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
