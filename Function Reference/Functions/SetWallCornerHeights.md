# SetWallCornerHeights

## Description
Sets the corner heights of a wall or round wall.

```pascal
FUNCTION SetWallCornerHeights(
				theWall           : HANDLE;
				startHeightTop    : REAL;
				startHeightBottom : REAL;
				endHeightTop      : REAL;
				endHeightBottom   : REAL): BOOLEAN;
```

```python
def vs.SetWallCornerHeights(theWall, startHeightTop, startHeightBottom, endHeightTop, endHeightBottom):
    return BOOLEAN
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
[GetWallCornerHeights](GetWallCornerHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
