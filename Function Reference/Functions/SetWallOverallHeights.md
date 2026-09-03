# SetWallOverallHeights

## Description
Sets the overall heights of a wall or round wall.

```pascal
FUNCTION SetWallOverallHeights(
				theWall           : HANDLE;
				botBoundType      : INTEGER;
				botBoundStory     : INTEGER;
				botLayerLevelType : STRING;
				botOffset         : REAL;
				topBoundType      : INTEGER;
				topBoundStory     : INTEGER;
				topLayerLevelType : STRING;
				topOffset         : REAL): BOOLEAN;
```

```python
def vs.SetWallOverallHeights(theWall, botBoundType, botBoundStory, botLayerLevelType, botOffset, topBoundType, topBoundStory, topLayerLevelType, topOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall or round wall|
|botBoundType|INTEGER|The type of the bottom bound||0 - Layer Z; 1 - Default Wall Height; 2 - Story|
|botBoundStory|INTEGER|The story of the bottom bound||0 - Object's story; 1 -  Story above; 2 - Story below|
|botLayerLevelType|STRING|The layer level type of the bottom bound|
|botOffset|REAL|The offset of the bottom bound|
|topBoundType|INTEGER|The type of the top bound||0 - Layer Z; 1 - Default Wall Height; 2 - Story|
|topBoundStory|INTEGER|The story of the top bound||0 - Object's story; 1 -  Story above; 2 - Story below|
|topLayerLevelType|STRING|The layer level type of the top bound|
|topOffset|REAL|The offset of the top bound|

## Examples
```pascal
SetObjExpandTexture(lNewObj,FALSE);
SetTextureRef(lNewObj,-1,7);
WallCap(FALSE,FALSE,FALSE,-3*upi,3*upi);
WallCap(TRUE,FALSE,FALSE,3*upi,-3*upi);
result := SetWallOverallHeights(lnewobj,0,0,'',cHeight,0,0,'',cHeight);
WallPeak((cWidth/2-3*upi),cRise+cHeight);
ResetObject(lNewObj);

BEGIN
	wallH1 := wallH [i];
	SetSelect (wallH1);
	IF (NOT useStyle) & (NOT useHeight) THEN
		OK := SetWallOverallHeights(wallH1,0,0,'',0,0,0,'',deltaZ);
```
```python
import vs

# Sets the overall heights of a wall or round wall.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer
botBoundType = 0
botBoundStory = 1
botLayerLevelType = 'Design Layer-1'
botOffset = 0.0
topBoundType = 0
topBoundStory = 2
topLayerLevelType = 'Design Layer-1'
topOffset = 0.0

ok = vs.SetWallOverallHeights(theWall, botBoundType, botBoundStory, botLayerLevelType, botOffset, topBoundType, topBoundStory, topLayerLevelType, topOffset)
if ok:
    vs.Message('SetWallOverallHeights succeeded')
else:
    vs.Message('SetWallOverallHeights failed')
```
See also in tutorials: [01. Draw a Room with Walls](ai%20examples/01_DrawRoomWithWalls.md), [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md)

## See Also
VS Functions:
[GetWallOverallHeights](GetWallOverallHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
