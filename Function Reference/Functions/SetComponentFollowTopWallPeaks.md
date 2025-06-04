# SetComponentFollowTopWallPeaks

## Description
Sets the follow top wall peaks flag of a component in an object.

```pascal
FUNCTION SetComponentFollowTopWallPeaks(
				obj                : HANDLE;
				componentIndex     : INTEGER;
				followTopWallPeaks : BOOLEAN): BOOLEAN;
```

```python
def vs.SetComponentFollowTopWallPeaks(obj, componentIndex, followTopWallPeaks):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|followTopWallPeaks|BOOLEAN|Whether or not the component will follow top wall peaks.|

## See Also
VS Functions:
[GetComponentFollowTopWallPeaks](GetComponentFollowTopWallPeaks.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
