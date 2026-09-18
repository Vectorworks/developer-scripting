# SetCompABoundEOffOff

## Description
Sets the auto-bound edge offset offset of a component in an object.

```pascal
FUNCTION SetCompABoundEOffOff(
				object                    : HANDLE;
				componentIndex            : INTEGER;
				autoBoundEdgeOffsetOffset : REAL (Coordinate)): BOOLEAN;
```

```python
def vs.SetCompABoundEOffOff(object, componentIndex, autoBoundEdgeOffsetOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a  slab, Slab Style, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|autoBoundEdgeOffsetOffset|REAL (Coordinate)|The auto-bound edge offset offset.|

## Examples
```pascal
SetCompABoundEOffOff(object, 1, 1.0);
```
```python
import vs

# Sets the auto-bound edge offset offset of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
autoBoundEdgeOffsetOffset = 0.0

ok = vs.SetCompABoundEOffOff(object, componentIndex, autoBoundEdgeOffsetOffset)
if ok:
    vs.Message('SetCompABoundEOffOff succeeded')
else:
    vs.Message('SetCompABoundEOffOff failed')
```

## See Also
VS Functions:
[GetCompABoundEOffOff](GetCompABoundEOffOff.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
