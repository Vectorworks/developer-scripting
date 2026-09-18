# GetComponentAutoBoundEdgeOffset

## Description
Gets the auto-bound edge offset of a component in an object.

```pascal
FUNCTION GetComponentAutoBoundEdgeOffset(
				obj                     : HANDLE;
				componentIndex          : INTEGER;
				VAR autoBoundEdgeOffset : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentAutoBoundEdgeOffset(obj, componentIndex):
    return (BOOLEAN, autoBoundEdgeOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a  slab, Slab Style, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|autoBoundEdgeOffset|INTEGER|Returns the auto-bound edge offset. 0 - Inner face, 1 - Outer face of inner component, 2 - Inner face of core, 3 - Center of core, 4 - Outer face of core, 5 - Inner face of outer component, 6 - Outer face|

## Examples
```pascal
resultOK := GetComponentAutoBoundEdgeOffset(obj, 1, 2);
```
```python
import vs

# Gets the auto-bound edge offset of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, autoBoundEdgeOffset = vs.GetComponentAutoBoundEdgeOffset(obj, componentIndex)
vs.Message('GetComponentAutoBoundEdgeOffset returned: ' + str((ok, autoBoundEdgeOffset)))
```

## See Also
VS Functions:
[SetComponentAutoBoundEdgeOffset](SetComponentAutoBoundEdgeOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
