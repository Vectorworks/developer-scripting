# PtPerpCircle

## Description
Returns a point on the circle which is closest to the input point.

```pascal
FUNCTION PtPerpCircle(
				pt     : VECTOR;
				cenPt  : VECTOR;
				radius : REAL): VECTOR;
```

```python
def vs.PtPerpCircle(pt, cenPt, radius):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt|VECTOR|   |
|cenPt|VECTOR|   |
|radius|REAL|   |

## Examples
```pascal
	pilaster_pt := PtPerpCircle(pilaster_pt, cntr_pt, radius);
	dDistAlongWall := DistAlongRoundWall( gWallHand, pilaster_pt.x, pilaster_pt.y, bIsOnWall );
END

IF cen_pt1 = cen_pt2 THEN BEGIN {! When would two points EVER be equal???}
	IF Abs(radius1 - radius2) < near_dist THEN BEGIN
		IF OverlapArc(cen_pt1, radius1, startAng1, sweepAng1, cen_pt2, radius2, startAng2, sweepAng2, lap_pt1, lap_pt2, fuzz) THEN BEGIN
			near_dist := Abs(radius1 - radius2);
			near_pt1 := PtPerpCircle(lap_pt1 + lap_pt2, cen_pt1, radius1);
			near_pt2 := PtPerpCircle(lap_pt1 + lap_pt2, cen_pt2, radius2);
		END;

{Shift lap_pt to a point on the segment, rather than off in space somewhere.}
IF vertices[spaces[sp_num].pts[vert_number]].tipe = 0
	then lap_pt := PtPerpLine(lap_pt, beg_pt, END_pt)
	ELSE lap_pt := PtPerpCircle(lap_pt, vertices[spaces[sp_num].pts[vert_number]].center, vertices[spaces[sp_num].pts[vert_number]].offset);
```
```python
import vs

# Returns a point on the circle which is closest to the input point.
pt = (0, 0)
cenPt = (1, 1)
radius = 1.0

vec = vs.PtPerpCircle(pt, cenPt, radius)
vs.Message('PtPerpCircle returned: ' + str(vec))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
