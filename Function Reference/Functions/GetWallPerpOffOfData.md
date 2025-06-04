# GetWallPerpOffOfData

## Description
Gets the perpendicular offset of an object in a wall from the insert data.

```pascal
FUNCTION GetWallPerpOffOfData(
				wall                 : HANDLE;
				insertLocation       : INTEGER;
				insertLocationOffset : REAL (Coordinate)): REAL;
```

```python
def vs.GetWallPerpOffOfData(wall, insertLocation, insertLocationOffset):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall.|
|insertLocation|INTEGER|The wall insert location.  -1 - Insert on the nearest edge of the wall 0 - Insert on the center of the wall 1 - Insert on the left edge of the wall 2 - Insert on the right edge of the wall 3 - Insert on the center of the wall core component 4 - Insert on the left edge of the wall core component 5 - Insert on the right edge of the wall core component 6 - Insert on the wall insert location 7 - Insert on the wall closure insert location|
|insertLocationOffset|REAL (Coordinate)|The wall insert location offset.|

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
