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

## Examples
```pascal
resultOK := SetWallCornerHeights(theWall, 1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Sets the corner heights of a wall or round wall.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer
startHeightTop = 2.0
startHeightBottom = 2.0
endHeightTop = 2.0
endHeightBottom = 2.0

ok = vs.SetWallCornerHeights(theWall, startHeightTop, startHeightBottom, endHeightTop, endHeightBottom)
if ok:
    vs.Message('SetWallCornerHeights succeeded')
else:
    vs.Message('SetWallCornerHeights failed')
```

## See Also
VS Functions:
[GetWallCornerHeights](GetWallCornerHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
