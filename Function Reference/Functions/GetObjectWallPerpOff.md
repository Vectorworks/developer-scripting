# GetObjectWallPerpOff

## Description
Gets the perpendicular offset of an object in a wall.

```pascal
FUNCTION GetObjectWallPerpOff(
				objectHandle            : HANDLE;
				wallHandle              : HANDLE;
				VAR perpendicularOffset : REAL): BOOLEAN;
```

```python
def vs.GetObjectWallPerpOff(objectHandle, wallHandle):
    return (BOOLEAN, perpendicularOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object in the wall.|
|wallHandle|HANDLE|The wall.|
|perpendicularOffset|REAL|Returns the perpendicular offset.|

## Examples
```pascal
resultOK := GetObjectWallPerpOff(objectHandle, wallHandle, 1.0);
```
```python
import vs

# Gets the perpendicular offset of an object in a wall.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
wallHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok, perpendicularOffset = vs.GetObjectWallPerpOff(objectHandle, wallHandle)
vs.Message('GetObjectWallPerpOff returned: ' + str((ok, perpendicularOffset)))
```

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
