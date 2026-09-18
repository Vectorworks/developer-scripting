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

## Examples
```pascal
	OK := JoinWalls (wallH1, wallH2, x, y, x1, y1, 4, FALSE, TRUE);
END;

	OK := JoinWalls (wallH1, wallH2, pt1.x, pt1.y, pt2.x, pt2.y, 2, FALSE, FALSE);
END;

	For I := 1 to NumPolyPoints - 2 DO BEGIN
		{check if the angle between walls to be joined is not too small for joining and join them}
		if CheckAngleBetweenWalls( I, I+1, I+2 ) then BEGIN
			PT1 := PolyPoints[I+1].pt;
			BS := JoinWalls(PolyPoints[I].h,PolyPoints[I+1].h,pt1.x,pt1.y,pt1.x,pt1.y,2,FALSE,FALSE);
{			DSelectAll;
			SetSelect( PolyPoints[I].h );
			SetSelect( PolyPoints[I+1].h );
			SetPref(12347, TRUE);
```
```python
import vs

# This function provides a VectorScript interface to the Wall Join Tool.
firstWall = vs.FSActLayer()  # handle to the first selected object on the active layer
secondWall = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
firstWallPt = (0, 0)
secondWallPt = (2, 2)
joinModifier = 1
capped = True
showAlerts = True

ok = vs.JoinWalls(firstWall, secondWall, firstWallPt, secondWallPt, joinModifier, capped, showAlerts)
if ok:
    vs.Message('JoinWalls succeeded')
else:
    vs.Message('JoinWalls failed')
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
