# GetWallCornerHeights

## Description
Gets the corner heights of a wall or round wall.

```pascal
PROCEDURE GetWallCornerHeights(
				theWall               : HANDLE;
				VAR startHeightTop    : REAL;
				VAR startHeightBottom : REAL;
				VAR endHeightTop      : REAL;
				VAR endHeightBottom   : REAL);
```

```python
def vs.GetWallCornerHeights(theWall):
    return (startHeightTop, startHeightBottom, endHeightTop, endHeightBottom)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall or round wall|
|startHeightTop|REAL|The height of the start top corner|
|startHeightBottom|REAL|The height of the start bottom corner|
|endHeightTop|REAL|The height of the end top corner|
|endHeightBottom|REAL|The height of the end bottom corner|

## See Also
VS Functions:
[SetWallCornerHeights](SetWallCornerHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
