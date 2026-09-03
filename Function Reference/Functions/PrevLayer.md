# PrevLayer

## Description
Function PrevLayer returns a handle to the layer in the document preceding the referenced layer.

```pascal
FUNCTION PrevLayer(h : HANDLE): HANDLE;
```

```python
def vs.PrevLayer(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Examples
```pascal
resultH := PrevLayer(h);
```
```python
import vs

# Function PrevLayer returns a handle to the layer in the document preceding
# the referenced layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.PrevLayer(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
