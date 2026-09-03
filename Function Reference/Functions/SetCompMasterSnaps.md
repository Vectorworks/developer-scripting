# SetCompMasterSnaps

## Description
Sets the master snaps of a component in an object.

```pascal
FUNCTION SetCompMasterSnaps(
				object            : HANDLE;
				componentIndex    : INTEGER;
				masterSnapOnLeft  : BOOLEAN;
				masterSnapOnRight : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompMasterSnaps(object, componentIndex, masterSnapOnLeft, masterSnapOnRight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|masterSnapOnLeft|BOOLEAN|Whether or not the component has a master snap on its left.|
|masterSnapOnRight|BOOLEAN|Whether or not the component has a master snap on its right.|

## Examples
```pascal
resultOK := SetCompMasterSnaps(object, 1, TRUE, FALSE);
```
```python
import vs

# Sets the master snaps of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
masterSnapOnLeft = True
masterSnapOnRight = True

ok = vs.SetCompMasterSnaps(object, componentIndex, masterSnapOnLeft, masterSnapOnRight)
if ok:
    vs.Message('SetCompMasterSnaps succeeded')
else:
    vs.Message('SetCompMasterSnaps failed')
```

## See Also
VS Functions:
[GetCompMasterSnaps](GetCompMasterSnaps.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
