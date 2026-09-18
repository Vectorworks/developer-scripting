# GetNumOfWallBreaks

## Description
Gets the number of breaks in a wall.

```pascal
FUNCTION GetNumOfWallBreaks(
				wallH             : HANDLE;
				VAR numWallBreaks : INTEGER): BOOLEAN;
```

```python
def vs.GetNumOfWallBreaks(wallH):
    return (BOOLEAN, numWallBreaks)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallH|HANDLE|   |
|numWallBreaks|INTEGER|   |

## Remarks
This currently fails on Round Walls. (VW 13.01+).

## Examples
```pascal
if (GetNumOfWallBreaks(originalWall_h, numOfBreaks) = true) then BEGIN
	for temp1_i := 0 to numOfBreaks DO BEGIN
		if (GetWallHalfBreakInfo(originalWall_h, temp1_i, breakStartPt.x, breakStartPt.y, breakCenterPt.x, breakCenterPt.y, breakEndPt.x, breakEndPt.y) = true) then BEGIN
			tJoinIsUnique := TRUE;
			if (dimToWallExts = TRUE) then BEGIN
				breakTestPt := breakStartPt;
			END ELSE BEGIN
				breakTestPt := breakCenterPt;
```
```python
import vs

# Gets the number of breaks in a wall.
wallH = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, numWallBreaks = vs.GetNumOfWallBreaks(wallH)
vs.Message('GetNumOfWallBreaks returned: ' + str((ok, numWallBreaks)))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
