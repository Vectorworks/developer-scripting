# PtPerpLine

## Description
Returns a point on the input line which is closest to the input point. Doesn't check to see that the point is ON the line.

```pascal
FUNCTION PtPerpLine(
				pt    : VECTOR;
				begPt : VECTOR;
				endPt : VECTOR): VECTOR;
```

```python
def vs.PtPerpLine(pt, begPt, endPt):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt|VECTOR|   |
|begPt|VECTOR|   |
|endPt|VECTOR|   |

## Examples
```pascal
	pilaster_pt := PtPerpCircle(pilaster_pt, cntr_pt, radius);
	dDistAlongWall := DistAlongRoundWall( gWallHand, pilaster_pt.x, pilaster_pt.y, bIsOnWall );
END
ELSE BEGIN
	pilaster_pt := PtPerpLine(pilaster_pt, begwall_pt, endwall_pt);
	dDistAlongWall := Distance(begwall_pt.x, begwall_pt.y, pilaster_pt.x, pilaster_pt.y);
END;

BEGIN
	DistPointPerp 	:= PtPerpLine( pts[cnt+1], pts[cnt-1], pts[cnt] );
	rowDistance 	:= (pts[cnt+1] - DistPointPerp);
	cntRow2 		:= cnt + 1;

beg_pt.z := 0;
END_pt.x := pt[numVerts].x;
END_pt.y := pt[numVerts].y;
END_pt.z := 0;
r := PtPerpLine(pnt, beg_pt, END_pt);
gElevationLoc.X := r.x;
gElevationLoc.Y := r.y;
IF gMarker1Name = kSectionLine THEN
BEGIN
```
```python
import vs

# Returns a point on the input line which is closest to the input point.
pt = (0, 0)
begPt = (1, 1)
endPt = (2, 2)

vec = vs.PtPerpLine(pt, begPt, endPt)
vs.Message('PtPerpLine returned: ' + str(vec))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
