# SetComponentAutoBoundEdgeOffset

## Description
Sets the auto-bound edge offset of a component in an object.

```pascal
FUNCTION SetComponentAutoBoundEdgeOffset(
				obj                 : HANDLE;
				componentIndex      : INTEGER;
				autoBoundEdgeOffset : INTEGER): BOOLEAN;
```

```python
def vs.SetComponentAutoBoundEdgeOffset(obj, componentIndex, autoBoundEdgeOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a  slab, Slab Style, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|autoBoundEdgeOffset|INTEGER|The auto-bound edge offset. 0 - Inner face, 1 - Outer face of inner component, 2 - Inner face of core, 3 - Center of core, 4 - Outer face of core, 5 - Inner face of outer component, 6 - Outer face|

## Examples
```pascal
resultOK := SetComponentAutoBoundEdgeOffset(obj, 1, 2);
```
```python
import vs

# Sets the auto-bound edge offset of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
autoBoundEdgeOffset = 1

ok = vs.SetComponentAutoBoundEdgeOffset(obj, componentIndex, autoBoundEdgeOffset)
if ok:
    vs.Message('SetComponentAutoBoundEdgeOffset succeeded')
else:
    vs.Message('SetComponentAutoBoundEdgeOffset failed')
```

## See Also
VS Functions:
[GetComponentAutoBoundEdgeOffset](GetComponentAutoBoundEdgeOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
