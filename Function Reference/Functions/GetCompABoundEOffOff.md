# GetCompABoundEOffOff

## Description
Gets the auto-bound edge offset offset of a component in an object.

```pascal
FUNCTION GetCompABoundEOffOff(
				object                        : HANDLE;
				componentIndex                : INTEGER;
				VAR autoBoundEdgeOffsetOffset : REAL): BOOLEAN;
```

```python
def vs.GetCompABoundEOffOff(object, componentIndex):
    return (BOOLEAN, autoBoundEdgeOffsetOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a  slab, Slab Style, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|autoBoundEdgeOffsetOffset|REAL|Returns the auto-bound edge offset offset.|

## Examples
```pascal
resultOK := GetCompABoundEOffOff(object, 1, 1.0);
```
```python
import vs

# Gets the auto-bound edge offset offset of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, autoBoundEdgeOffsetOffset = vs.GetCompABoundEOffOff(object, componentIndex)
vs.Message('GetCompABoundEOffOff returned: ' + str((ok, autoBoundEdgeOffsetOffset)))
```

## See Also
VS Functions:
[SetCompABoundEOffOff](SetCompABoundEOffOff.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
