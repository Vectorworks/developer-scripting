# GetWallRecessGroup

## Description
Get the wall recess geometry group associated with the object.

```pascal
FUNCTION GetWallRecessGroup(objectHand : HANDLE): HANDLE;
```

```python
def vs.GetWallRecessGroup(objectHand):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Object handle to get the geometry for.|

## Examples
```pascal
resultH := GetWallRecessGroup(objectHand);
```
```python
import vs

# Get the wall recess geometry group associated with the object.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetWallRecessGroup(objectHand)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
