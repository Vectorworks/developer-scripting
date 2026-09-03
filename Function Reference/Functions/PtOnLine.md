# PtOnLine

## Description
Determines if a point is on a line.

```pascal
FUNCTION PtOnLine(
				pt        : VECTOR;
				begPt     : VECTOR;
				endPt     : VECTOR;
				tolerance : REAL): BOOLEAN;
```

```python
def vs.PtOnLine(pt, begPt, endPt, tolerance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt|VECTOR|   |
|begPt|VECTOR|   |
|endPt|VECTOR|   |
|tolerance|REAL|   |

## Examples
```pascal
found1 := FALSE; found2 := FALSE;
tempV[1] := BBVec2[1]; tempV[2] := BBVec1[2];
if IntersLineLine( originVec, realBBV1, BBVec1, tempV, intersV ) then BEGIN
	{check whether the intersection point lies on the BBox segment}
	if PtOnLine( intersV, BBVec1, tempV, kPtOnLinePrecision*gUPI ) then BEGIN
		realV1 := intersV; found1 := TRUE;
	END;

IF ( cnt + 1)  < pts_cnt THEN
IF NOT PtOnLine(pts[cnt+1],pts[cnt],pts[cnt+2],1") THEN
BEGIN
	hght 	:= hght + pRise;
	RowNum 	:= RowNum + 1;
END;

{ sometimes here happens distortion. try to correct X and Y of the new pt. }
corrXYpt := PtPerpLine( newPt, RailPts[ptCnt1-1], RailPts[ptCnt1] );
IF ( PtOnLine( corrXYPt, RailPts[ptCnt1-1], RailPts[ptCnt1], fuzz ) ) THEN BEGIN
	newPt.x := corrXYpt.x;
	newPt.y := corrXYpt.y;
END;
```
```python
import vs

# Determines if a point is on a line.
pt = (0, 0)
begPt = (1, 1)
endPt = (2, 2)
tolerance = 1.0

ok = vs.PtOnLine(pt, begPt, endPt, tolerance)
if ok:
    vs.Message('PtOnLine succeeded')
else:
    vs.Message('PtOnLine failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
