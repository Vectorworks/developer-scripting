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

## Examples
```pascal
BEGIN
IF (GetType(selWall)=68) OR (GetType(selWall)=89) THEN BEGIN
	selLength:=HLength(selWall);
	GetWallCornerHeights(selWall,startHeightTop,startHeightBottom,endHeightTop,endHeightBottom);
	selHeight1 := startHeightTop-startHeightBottom;
	selHeight2 := endHeightTop-endHeightBottom;
	IF selHeight1<>selHeight2
		THEN selHeight:=kVaries
```
```python
import vs

# Gets the corner heights of a wall or round wall.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer

startHeightTop, startHeightBottom, endHeightTop, endHeightBottom = vs.GetWallCornerHeights(theWall)
vs.Message('GetWallCornerHeights returned: ' + str((startHeightTop, startHeightBottom, endHeightTop, endHeightBottom)))
```

## See Also
VS Functions:
[SetWallCornerHeights](SetWallCornerHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
