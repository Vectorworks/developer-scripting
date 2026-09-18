# SetCompManualBound

## Description
Sets the manual bound of a component in an object.

```pascal
FUNCTION SetCompManualBound(
				object         : HANDLE;
				componentIndex : INTEGER;
				manualBound    : INTEGER): BOOLEAN;
```

```python
def vs.SetCompManualBound(object, componentIndex, manualBound):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|manualBound|INTEGER|The manual bound of the component.  0 - Roof edge 1 - Roof axis line|

## Examples
```pascal
resultOK := SetCompManualBound(object, 1, 2);
```
```python
import vs

# Sets the manual bound of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
manualBound = 1

ok = vs.SetCompManualBound(object, componentIndex, manualBound)
if ok:
    vs.Message('SetCompManualBound succeeded')
else:
    vs.Message('SetCompManualBound failed')
```

## See Also
VS Functions:
[GetCompManualBound](GetCompManualBound.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
