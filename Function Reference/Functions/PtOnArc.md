# PtOnArc

## Description
Determines if a point is on an arc.

```pascal
FUNCTION PtOnArc(
				pt        : VECTOR;
				cenPt     : VECTOR;
				radius    : REAL;
				startAng  : REAL;
				sweepAng  : REAL;
				tolerance : REAL): BOOLEAN;
```

```python
def vs.PtOnArc(pt, cenPt, radius, startAng, sweepAng, tolerance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt|VECTOR|   |
|cenPt|VECTOR|   |
|radius|REAL|   |
|startAng|REAL|   |
|sweepAng|REAL|   |
|tolerance|REAL|   |

## Examples
```pascal
BEGIN
	pt1.z := 0; pt2.z := 0;
	IF LineCircleIntersect(beg_pt, end_pt, cen_pt, rad, pt1, pt2) THEN BEGIN
		IF PtOnArc(pt1, cen_pt, rad, startAng, sweepAng, fuzz) THEN pt1.z := 1;
		IF PtOnArc(pt2, cen_pt, rad, startAng, sweepAng, fuzz) THEN pt2.z := 1;
	END;

IF (PtOnArc(pt, cntr_pt, radius, startAng, sweepAng, fuzz)) THEN BEGIN

	{ check if clockwise }
	if (GetObjectVariableBoolean(WallH, 570)) then BEGIN
		GetSegPt1(WallH, beg_pt.x, beg_pt.y);
	end else BEGIN
		GetSegPt2(WallH, beg_pt.x, beg_pt.y);
	END;

cenPt.y  := verts[cnt, 7];
startAng := verts[cnt, 8];
sweepAng := verts[cnt, 9];
IF LineCircleIntersect(begPt, endPt, cenPt, radius, pt1, pt2) THEN BEGIN
	IF PtOnArc(pt1, cenPt, radius, startAng, sweepAng, fuzz^2) THEN StowIt(pt1);
	IF PtOnArc(pt2, cenPt, radius, startAng, sweepAng, fuzz^2) THEN StowIt(pt2);
END;
```
```python
import vs

# Determines if a point is on an arc.
pt = (0, 0)
cenPt = (1, 1)
radius = 1.0
startAng = 1.0
sweepAng = 2.0
tolerance = 0.5

ok = vs.PtOnArc(pt, cenPt, radius, startAng, sweepAng, tolerance)
if ok:
    vs.Message('PtOnArc succeeded')
else:
    vs.Message('PtOnArc failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
