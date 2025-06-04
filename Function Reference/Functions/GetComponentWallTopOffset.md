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

## See Also
VS Functions:
[SetComponentWallTopOffset](SetComponentWallTopOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
