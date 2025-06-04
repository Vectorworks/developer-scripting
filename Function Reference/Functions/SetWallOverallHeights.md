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

## See Also
VS Functions:
[GetWallOverallHeights](GetWallOverallHeights.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
