# SetComponentWallBottomOffset

## Description
Sets the offset from wall bottom of a component in an object.

```pascal
FUNCTION SetComponentWallBottomOffset(
				obj                  : HANDLE;
				componentIndex       : INTEGER;
				offsetFromWallBottom : REAL): BOOLEAN;
```

```python
def vs.SetComponentWallBottomOffset(obj, componentIndex, offsetFromWallBottom):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|offsetFromWallBottom|REAL|The offset from wall bottom of the component.|

## Examples
```pascal
resultOK := SetComponentWallBottomOffset(obj, 1, 1.0);
```
```python
import vs

# Sets the offset from wall bottom of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
offsetFromWallBottom = 0.0

ok = vs.SetComponentWallBottomOffset(obj, componentIndex, offsetFromWallBottom)
if ok:
    vs.Message('SetComponentWallBottomOffset succeeded')
else:
    vs.Message('SetComponentWallBottomOffset failed')
```

## See Also
VS Functions:
[GetComponentWallBottomOffset](GetComponentWallBottomOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
