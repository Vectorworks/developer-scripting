# JoinWalls

## Description
This function provides a VectorScript interface to the Wall Join Tool. The parameters firstWall and secondWall are used to specify the pick points that determine which ends of the walls are to be joined, similar to the points requested by the Wall Join Tool.

```pascal
FUNCTION JoinWalls(
				firstWall               : HANDLE;
				secondWall              : HANDLE;
				firstWallX,firstWallY   : REAL;
				secondWallX,secondWallY : REAL;
				joinModifier            : INTEGER;
				capped                  : BOOLEAN;
				showAlerts              : BOOLEAN): BOOLEAN;
```

```python
def vs.JoinWalls(firstWall, secondWall, firstWallPt, secondWallPt, joinModifier, capped, showAlerts):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|firstWall|HANDLE|The first wall of the join operation. For T joins this is the wall that is extended to meet the second wall.|
|secondWall|HANDLE|The second wall of the join operation.|
|firstWallPt|REAL|The first and second wall points are used to clarify corner joins.|
|secondWallPt|REAL|The first and second wall points are used to clarify corner joins.|
|joinModifier|INTEGER|Specifies the type of join: T-join = 1, L-join = 2, X-join = 3, and auto join = 4.|
|capped|BOOLEAN|True for capped joins, false for un-capped joins.|
|showAlerts|BOOLEAN|Show an alert dialog if the join operation fails.|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
