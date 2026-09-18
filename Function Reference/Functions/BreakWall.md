# BreakWall

## Description
Procedure BreakWall creates a break in a wall object on the left or the right at a specified offset location.

```pascal
PROCEDURE BreakWall(
				offsetDistance     : REAL;
				breakWidthDistance : REAL;
				right              : BOOLEAN);
```

```python
def vs.BreakWall(offsetDistance, breakWidthDistance, right):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|offsetDistance|REAL|Offset distance from wall start.|
|breakWidthDistance|REAL|Width of wall break.|
|right|BOOLEAN|Left-right edge status of break.|

## Examples
#### VectorScript ####
```pascal
MoveTo(2,3);
WallTo(7,3);
BreakWall(3&quot;,1&quot;,True);
{creates a right hand 1&quot; wall break 3&quot; from the start of the wall}
```
#### Python ####
```python
vs.MoveTo(2,3)
vs.WallTo(7,3)
vs.BreakWall(3,1,True)
```

```pascal
BreakWall(1.0, 2.0, TRUE);
```
```python
import vs

# Procedure BreakWall creates a break in a wall object on the left or the
# right at a specified offset location.
offsetDistance = 1.0
breakWidthDistance = 2.0
right = True

vs.BreakWall(offsetDistance, breakWidthDistance, right)
```

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
