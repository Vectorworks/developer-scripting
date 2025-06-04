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

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
