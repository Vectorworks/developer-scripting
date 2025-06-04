# SetObjWallInsertMode

## Description
Set the insertion mode for an object in a wall.<BR>
<BR>
1 - Center<BR>
2 - Leaf Edge<BR>
3 - Right Edge<BR>
<BR>
<BR>
The object (objH) must be contained in wall (wallH)  to succeed.

```pascal
FUNCTION SetObjWallInsertMode(
				objH       : HANDLE;
				wallH      : HANDLE;
				insertMode : INTEGER): Boolean;
```

```python
def vs.SetObjWallInsertMode(objH, wallH, insertMode):
    return Boolean
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|insertMode|INTEGER|   |

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
