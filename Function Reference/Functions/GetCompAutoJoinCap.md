# GetCompAutoJoinCap

## Description
Gets the always auto join in Capped Join mode flag of a component in an object.

```pascal
FUNCTION GetCompAutoJoinCap(
				object                             : HANDLE;
				componentIndex                     : INTEGER;
				VAR alwaysAutoJoinInCappedJoinMode : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompAutoJoinCap(object, componentIndex):
    return (BOOLEAN, alwaysAutoJoinInCappedJoinMode)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|alwaysAutoJoinInCappedJoinMode|BOOLEAN|Returns whether or not the component always auto joins in Capped Join mode.|

## Examples
```pascal
resultOK := GetCompAutoJoinCap(object, 1, TRUE);
```
```python
import vs

# Gets the always auto join in Capped Join mode flag of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, alwaysAutoJoinInCappedJoinMode = vs.GetCompAutoJoinCap(object, componentIndex)
vs.Message('GetCompAutoJoinCap returned: ' + str((ok, alwaysAutoJoinInCappedJoinMode)))
```

## See Also
VS Functions:
[SetCompAutoJoinCap](SetCompAutoJoinCap.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
