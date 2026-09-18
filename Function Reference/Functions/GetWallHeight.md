# GetWallHeight

## Description
Returns the height at the start and at the end of a wall.

```pascal
PROCEDURE GetWallHeight(
				hWall             : HANDLE;
				VAR dStartTopHght : REAL;
				VAR dStartBotHght : REAL;
				VAR dEndTopHght   : REAL;
				VAR dEndBotHght   : REAL);
```

```python
def vs.GetWallHeight(hWall):
    return (dStartTopHght, dStartBotHght, dEndTopHght, dEndBotHght)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hWall|HANDLE|   |
|dStartTopHght|REAL|   |
|dStartBotHght|REAL|   |
|dEndTopHght|REAL|   |
|dEndBotHght|REAL|   |

## Examples
```pascal
{from 3D to 2D coordinate system}
GetWallHeight(WallH, dTop1H, dBottom1H, dTop2H, dBottom2H);
dBottom1L		:= 0;
dBottom2L		:= dDistTemp;

GetWallHeight(WallHand, dTop1H, dBottom1H, dTop2H, dBottom2H);
```
```python
import vs

# Returns the height at the start and at the end of a wall.
hWall = vs.FSActLayer()  # handle to the first selected object on the active layer

dStartTopHght, dStartBotHght, dEndTopHght, dEndBotHght = vs.GetWallHeight(hWall)
vs.Message('GetWallHeight returned: ' + str((dStartTopHght, dStartBotHght, dEndTopHght, dEndBotHght)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
