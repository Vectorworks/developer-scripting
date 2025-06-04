# WallCap

## Description
Procedure WallCap creates a wall cap on a newly created wall object.

Specifying nonzero values for the cap offset values will create angled wall caps.

```pascal
PROCEDURE WallCap(
				atStart          : BOOLEAN;
				closed           : BOOLEAN;
				round            : BOOLEAN;
				rightOffDistance : REAL;
				leftOffDistance  : REAL);
```

```python
def vs.WallCap(atStart, closed, round, rightOffDistance, leftOffDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|atStart|BOOLEAN|Start-end location of wall cap.|
|closed|BOOLEAN|Controls display status of cap.|
|round|BOOLEAN|Specifies flat or round cap.|
|rightOffDistance|REAL|Right extension of wall line beyond end point.|
|leftOffDistance|REAL|Left extension of wall line beyond end point.|

## Examples
#### VectorScript ####
```pascal
Wall(0,0,7',0);
WallCap(True, True, False, 1.0', 0.0);
{sets the cap status of the starting cap of the wall as flat cap, bevelled, with the right side extending 1' beyond the wall end point}
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
