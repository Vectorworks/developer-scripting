# GetObjWallBreakMode

## Description
Returns the break mode for an object in a wall.<BR>
<BR>
1 - Full Break with Caps<BR>
2 - Full Break no Caps<BR>
3 - Half Break<BR>
4 - No Break<BR>
<BR>
The object (objH) must be contained in wall (wallH)  to succeed.

```pascal
FUNCTION GetObjWallBreakMode(
				objH          : HANDLE;
				wallH         : HANDLE;
				VAR breakMode : INTEGER): Boolean;
```

```python
def vs.GetObjWallBreakMode(objH, wallH, breakMode):
    return (Boolean, breakMode)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|breakMode|INTEGER|   |

## Examples
```pascal
resultOK := GetObjWallBreakMode(objH, wallH, 1);
```
```python
import vs

# Returns the break mode for an object in a wall.
objH = vs.FSActLayer()  # handle to the first selected object on the active layer
wallH = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
breakMode = 0

ok, breakMode = vs.GetObjWallBreakMode(objH, wallH, breakMode)
vs.Message('GetObjWallBreakMode returned: ' + str((ok, breakMode)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
