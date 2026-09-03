# SetCompAutoJoinCap

## Description
Sets the always auto join in Capped Join mode flag of a component in an object.

```pascal
FUNCTION SetCompAutoJoinCap(
				object                         : HANDLE;
				componentIndex                 : INTEGER;
				alwaysAutoJoinInCappedJoinMode : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompAutoJoinCap(object, componentIndex, alwaysAutoJoinInCappedJoinMode):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|alwaysAutoJoinInCappedJoinMode|BOOLEAN|Whether or not the component always auto joins in Capped Join mode.|

## Examples
```pascal
resultOK := SetCompAutoJoinCap(object, 1, TRUE);
```
```python
import vs

# Sets the always auto join in Capped Join mode flag of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
alwaysAutoJoinInCappedJoinMode = True

ok = vs.SetCompAutoJoinCap(object, componentIndex, alwaysAutoJoinInCappedJoinMode)
if ok:
    vs.Message('SetCompAutoJoinCap succeeded')
else:
    vs.Message('SetCompAutoJoinCap failed')
```

## See Also
VS Functions:
[GetCompAutoJoinCap](GetCompAutoJoinCap.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
