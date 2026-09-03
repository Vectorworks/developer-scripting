# SetCompBoundOffset

## Description
Sets the bound offset of a component in an object.

```pascal
FUNCTION SetCompBoundOffset(
				object         : HANDLE;
				componentIndex : INTEGER;
				boundOffset    : REAL): BOOLEAN;
```

```python
def vs.SetCompBoundOffset(object, componentIndex, boundOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|boundOffset|REAL|The bound offset of the component.|

## Examples
```pascal
resultOK := SetCompBoundOffset(object, 1, 1.0);
```
```python
import vs

# Sets the bound offset of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
boundOffset = 0.0

ok = vs.SetCompBoundOffset(object, componentIndex, boundOffset)
if ok:
    vs.Message('SetCompBoundOffset succeeded')
else:
    vs.Message('SetCompBoundOffset failed')
```

## See Also
VS Functions:
[GetCompBoundOffset](GetCompBoundOffset.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
