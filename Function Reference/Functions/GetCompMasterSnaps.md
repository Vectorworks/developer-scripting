# GetCompMasterSnaps

## Description
Gets the master snaps of a component in an object.

```pascal
FUNCTION GetCompMasterSnaps(
				object                : HANDLE;
				componentIndex        : INTEGER;
				VAR masterSnapOnLeft  : BOOLEAN;
				VAR masterSnapOnRight : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompMasterSnaps(object, componentIndex):
    return (BOOLEAN, masterSnapOnLeft, masterSnapOnRight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|masterSnapOnLeft|BOOLEAN|Returns whether or not the component has a master snap on its left.|
|masterSnapOnRight|BOOLEAN|Returns whether or not the component has a master snap on its right.|

## See Also
VS Functions:
[SetCompMasterSnaps](SetCompMasterSnaps.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
