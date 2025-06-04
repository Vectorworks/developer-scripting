# GetObjectWallHeight

## Description
Gets an object's height value in it's break record. <BR>
<BR>
The object (objH) must be contained in wall (wallH)  to succeed.

```pascal
FUNCTION GetObjectWallHeight(
				objH       : HANDLE;
				wallH      : HANDLE;
				VAR height : REAL): BOOLEAN;
```

```python
def vs.GetObjectWallHeight(objH, wallH):
    return (BOOLEAN, height)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|height|REAL|   |

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
