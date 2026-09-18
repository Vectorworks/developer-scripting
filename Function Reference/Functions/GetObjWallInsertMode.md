# GetObjWallInsertMode

## Description
Returns the insertion mode for an object in a wall.<BR>
<BR>
0 - Wall - Centerline<BR>
1 - Wall - Left Edge<BR>
2 - Wall - Right Edge<BR>
3 - Core Component - Centerline<BR>
4 - Core Component - Left Edge<BR>
5 - Core Component - Right Edge<BR>
<BR>
The object (objH) must be contained in wall (wallH)  to succeed.

```pascal
FUNCTION GetObjWallInsertMode(
				objH           : HANDLE;
				wallH          : HANDLE;
				VAR insertMode : INTEGER): Boolean;
```

```python
def vs.GetObjWallInsertMode(objH, wallH, insertMode):
    return (Boolean, insertMode)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|insertMode|INTEGER|   |

## Remarks
[[User:Ptr|Ptr]] 2022.07.01:
In Python the third parameter (insertMode) doesn't do anything, but it needs to be entered to avoid an error message.

## Examples
```pascal
resultOK := GetObjWallInsertMode(objH, wallH, 1);
```
```python
import vs

# Returns the insertion mode for an object in a wall.
objH = vs.FSActLayer()  # handle to the first selected object on the active layer
wallH = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
insertMode = 0

ok, insertMode = vs.GetObjWallInsertMode(objH, wallH, insertMode)
vs.Message('GetObjWallInsertMode returned: ' + str((ok, insertMode)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
