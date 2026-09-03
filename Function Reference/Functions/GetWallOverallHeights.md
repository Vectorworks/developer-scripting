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

## Examples
```pascal
BEGIN
Get3DInfo(hobj,dp,wd,ht);
Get3DCntr(hobj,x,y,z);
IF (IsLineBasedWall(hwall)) THEN
	GetWallOverallHeights(hwall,wallh1,wallh2)
ELSE IF IsArcBasedWall(hWall) THEN BEGIN { roundwall condition }
	Get3DInfo(hwall,wt,ww,wh);
	wallh1 := wh;
	wallh2 := wh;
END;
```
```python
import vs

# Gets the overall heights of a wall or round wall.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer

overallHeightTop, overallHeightBottom = vs.GetWallOverallHeights(theWall)
vs.Message('GetWallOverallHeights returned: ' + str((overallHeightTop, overallHeightBottom)))
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md)

## See Also
VS Functions:
[SetWallOverallHeights](SetWallOverallHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
