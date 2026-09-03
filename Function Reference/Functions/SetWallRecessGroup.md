# SetWallRecessGroup

## Description
Set the wall recess geometry group associated with the object.

```pascal
PROCEDURE SetWallRecessGroup(
				objectHand    : HANDLE;
				geometryGroup : HANDLE);
```

```python
def vs.SetWallRecessGroup(objectHand, geometryGroup):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Object handle to set the geometry for.|
|geometryGroup|HANDLE|The group containing the new geometry.|

## Examples
```pascal
SetWallRecessGroup(objectHand, geometryGroup);
```
```python
import vs

# Set the wall recess geometry group associated with the object.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer
geometryGroup = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.SetWallRecessGroup(objectHand, geometryGroup)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
