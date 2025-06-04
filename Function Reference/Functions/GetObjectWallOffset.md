# GetObjectWallOffset

## Description
Gets an object's offset value in it's break record.

The object (objH) must be contained in wall (wallH) to succeed.

```pascal
FUNCTION GetObjectWallOffset(
				objH       : HANDLE;
				wallH      : HANDLE;
				VAR offset : REAL): BOOLEAN;
```

```python
def vs.GetObjectWallOffset(objH, wallH):
    return (BOOLEAN, offset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|offset|REAL|   |

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
