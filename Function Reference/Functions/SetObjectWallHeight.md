# SetObjectWallHeight

## Description
Sets an object's height value in it's break record.

The object (objH) must be contained in wall (wallH)  to succeed.

```pascal
FUNCTION SetObjectWallHeight(
				objH   : HANDLE;
				wallH  : HANDLE;
				height : REAL (Coordinate)): BOOLEAN;
```

```python
def vs.SetObjectWallHeight(objH, wallH, height):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|height|REAL (Coordinate)|   |

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
