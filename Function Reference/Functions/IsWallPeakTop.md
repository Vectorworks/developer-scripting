# IsWallPeakTop

## Description
Returns true if specified peak (by index) of a wall is top.

```pascal
FUNCTION IsWallPeakTop(
				hWall     : HANDLE;
				peakIndex : INTEGER): BOOLEAN;
```

```python
def vs.IsWallPeakTop(hWall, peakIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hWall|HANDLE|   |
|peakIndex|INTEGER|   |

## Examples
```pascal
IF (NOT IsWallPeakTop(WallH, i)) THEN BEGIN
	IF NOT bBottomPrep THEN BEGIN
		IF (dDistTemp < dDist) THEN BEGIN
			dBottom1L	:= dDistTemp;
			dBottom1H	:= peak_pt.z;
		END ELSE BEGIN
			dBottom2L	:= dDistTemp;
			dBottom2H	:= peak_pt.z;
```
```python
import vs

# Returns true if specified peak (by index) of a wall is top.
hWall = vs.FSActLayer()  # handle to the first selected object on the active layer
peakIndex = 1

ok = vs.IsWallPeakTop(hWall, peakIndex)
if ok:
    vs.Message('IsWallPeakTop succeeded')
else:
    vs.Message('IsWallPeakTop failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
