# SetComponentManualEdgeOffset

## Description
Sets the manual edge offset of a component in an object.

```pascal
FUNCTION SetComponentManualEdgeOffset(
				obj              : HANDLE;
				componentIndex   : INTEGER;
				manualEdgeOffset : REAL): BOOLEAN;
```

```python
def vs.SetComponentManualEdgeOffset(obj, componentIndex, manualEdgeOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a  slab, Slab Style, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|manualEdgeOffset|REAL|The manual edge offset.|

## Examples
```pascal
resultOK := SetComponentManualEdgeOffset(obj, 1, 1.0);
```
```python
import vs

# Sets the manual edge offset of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
manualEdgeOffset = 0.0

ok = vs.SetComponentManualEdgeOffset(obj, componentIndex, manualEdgeOffset)
if ok:
    vs.Message('SetComponentManualEdgeOffset succeeded')
else:
    vs.Message('SetComponentManualEdgeOffset failed')
```

## See Also
VS Functions:
[GetComponentManualEdgeOffset](GetComponentManualEdgeOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
