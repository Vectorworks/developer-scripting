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

## Examples
```pascal
resultOK := SetObjWallInsertMode(objH, wallH, 1);
```
```python
import vs

# Set the insertion mode for an object in a wall.
objH = vs.FSActLayer()  # handle to the first selected object on the active layer
wallH = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
insertMode = 0

ok = vs.SetObjWallInsertMode(objH, wallH, insertMode)
if ok:
    vs.Message('SetObjWallInsertMode succeeded')
else:
    vs.Message('SetObjWallInsertMode failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
