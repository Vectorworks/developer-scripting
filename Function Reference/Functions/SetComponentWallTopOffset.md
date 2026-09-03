# SetComponentWallTopOffset

## Description
Sets the offset from wall top of a component in an object.

```pascal
FUNCTION SetComponentWallTopOffset(
				obj               : HANDLE;
				componentIndex    : INTEGER;
				offsetFromWallTop : REAL): BOOLEAN;
```

```python
def vs.SetComponentWallTopOffset(obj, componentIndex, offsetFromWallTop):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|offsetFromWallTop|REAL|The offset from wall top of the component.|

## Examples
```pascal
resultOK := SetComponentWallTopOffset(obj, 1, 1.0);
```
```python
import vs

# Sets the offset from wall top of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
offsetFromWallTop = 0.0

ok = vs.SetComponentWallTopOffset(obj, componentIndex, offsetFromWallTop)
if ok:
    vs.Message('SetComponentWallTopOffset succeeded')
else:
    vs.Message('SetComponentWallTopOffset failed')
```

## See Also
VS Functions:
[GetComponentWallTopOffset](GetComponentWallTopOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
