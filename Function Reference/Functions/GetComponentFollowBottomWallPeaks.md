# GetComponentFollowBottomWallPeaks

## Description
Gets the follow bottom wall peaks flag of a component in an object.

```pascal
FUNCTION GetComponentFollowBottomWallPeaks(
				obj                       : HANDLE;
				componentIndex            : INTEGER;
				VAR followBottomWallPeaks : BOOLEAN): BOOLEAN;
```

```python
def vs.GetComponentFollowBottomWallPeaks(obj, componentIndex):
    return (BOOLEAN, followBottomWallPeaks)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|followBottomWallPeaks|BOOLEAN|Returns whether or not the component is following bottom wall peaks.|

## Examples
```pascal
resultOK := GetComponentFollowBottomWallPeaks(obj, 1, TRUE);
```
```python
import vs

# Gets the follow bottom wall peaks flag of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, followBottomWallPeaks = vs.GetComponentFollowBottomWallPeaks(obj, componentIndex)
vs.Message('GetComponentFollowBottomWallPeaks returned: ' + str((ok, followBottomWallPeaks)))
```

## See Also
VS Functions:
[SetComponentFollowBottomWallPeaks](SetComponentFollowBottomWallPeaks.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
