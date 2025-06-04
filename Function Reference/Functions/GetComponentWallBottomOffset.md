# GetComponentWallBottomOffset

## Description
Gets the offset from wall bottom of a component in an object.

```pascal
FUNCTION GetComponentWallBottomOffset(
				obj                      : HANDLE;
				componentIndex           : INTEGER;
				VAR offsetFromWallBottom : REAL): BOOLEAN;
```

```python
def vs.GetComponentWallBottomOffset(obj, componentIndex):
    return (BOOLEAN, offsetFromWallBottom)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|offsetFromWallBottom|REAL|Returns the offset from wall bottom of the component.|

## See Also
VS Functions:
[SetComponentWallBottomOffset](SetComponentWallBottomOffset.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
