# GetComponentWallTopOffset

## Description
Gets the offset from wall top of a component in an object.

```pascal
FUNCTION GetComponentWallTopOffset(
				obj                   : HANDLE;
				componentIndex        : INTEGER;
				VAR offsetFromWallTop : REAL): BOOLEAN;
```

```python
def vs.GetComponentWallTopOffset(obj, componentIndex):
    return (BOOLEAN, offsetFromWallTop)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|offsetFromWallTop|REAL|Returns the offset from wall top of the component.|

## Examples
```pascal
resultOK := GetComponentWallTopOffset(obj, 1, 1.0);
```
```python
import vs

# Gets the offset from wall top of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, offsetFromWallTop = vs.GetComponentWallTopOffset(obj, componentIndex)
vs.Message('GetComponentWallTopOffset returned: ' + str((ok, offsetFromWallTop)))
```

## See Also
VS Functions:
[SetComponentWallTopOffset](SetComponentWallTopOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
