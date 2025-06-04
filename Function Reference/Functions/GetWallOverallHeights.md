# GetWallOverallHeights

## Description
Gets the overall heights of a wall or round wall.

```pascal
PROCEDURE GetWallOverallHeights(
				theWall                 : HANDLE;
				VAR overallHeightTop    : REAL;
				VAR overallHeightBottom : REAL);
```

```python
def vs.GetWallOverallHeights(theWall):
    return (overallHeightTop, overallHeightBottom)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall or round wall|
|overallHeightTop|REAL|The overall height of the top|
|overallHeightBottom|REAL|The overall height of the bottom|

## See Also
VS Functions:
[SetWallOverallHeights](SetWallOverallHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
