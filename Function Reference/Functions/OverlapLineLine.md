# OverlapLineLine

## Description
Returns two points the lap zone of two lines.

```pascal
FUNCTION OverlapLineLine(
				begPt1     : VECTOR;
				endPt1     : VECTOR;
				begPt2     : VECTOR;
				endPt2     : VECTOR;
				VAR lapPt1 : VECTOR;
				VAR lapPt2 : VECTOR;
				tolerance  : REAL): BOOLEAN;
```

```python
def vs.OverlapLineLine(begPt1, endPt1, begPt2, endPt2, tolerance):
    return (BOOLEAN, lapPt1, lapPt2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|begPt1|VECTOR|   |
|endPt1|VECTOR|   |
|begPt2|VECTOR|   |
|endPt2|VECTOR|   |
|lapPt1|VECTOR|   |
|lapPt2|VECTOR|   |
|tolerance|REAL|   |

## Examples
```pascal
pt1.x := holes[cnt1].beg_r;
pt2.x := holes[cnt1].END_r;
pt3.x := holes[cnt2].beg_r;
pt4.x := holes[cnt2].END_r;
IF OverlapLineLine(pt1, pt2, pt3, pt4, pt0, pt0, minHoleSep) THEN BEGIN
	pt1.x := 0;
	pt2.x := 0;
	pt3.x := 0;
	pt4.x := 0;
	pt1.y := holes[cnt1].bot_r;

	(EqPt2D(w1.END_pt,  w2.beg_pt, fuzzIntLap)) |
	(EqPt2D(w1.END_pt,  w2.END_pt, fuzzIntLap)) |
	(EqPt2D(w1.beg_pt,  w2.beg_pt, fuzzIntLap)) |
	(EqPt2D(w1.beg_pt,  w2.END_pt, fuzzIntLap)) |
	(OverlapLineLine(w1.beg_pt, w1.END_pt, w2.beg_pt, w2.END_pt, pt1, pt2, fuzzIntLap))
)
&
(
	(
		(EqSlope(w1.slope, w2.slope, startNewWallAfterAng)) &
		(Eq(w1.offset, w2.offset, fuzzIntJog))
	)

{OverlapLineLine returns the lap points -- the points defining the overlapping segment
common to both lines. If true (and if the overlapping segment is big enough to
worry about), you've got an "interior" segment.}
if OverlapLineLine(pt1, pt2, pt3, pt4, lap_pt1, lap_pt2, fuzz_lin) then BEGIN
	{Now you have to figure out if additional vertices need to be added to the polys,
	since it may be a partial overlap, and the only way to handle that is to add new
	vertices. First get them pointed in the right direction.}
	if dist(lap_pt1, pt1) > dist(lap_pt2, pt1) then BEGIN
		temp_pt := lap_pt1;
		lap_pt1 := lap_pt2;
		lap_pt2 := temp_pt;
	END;
```
```python
import vs

# Returns two points the lap zone of two lines.
begPt1 = (0, 0)
endPt1 = (1, 1)
begPt2 = (2, 2)
endPt2 = (0, 0)
tolerance = 1.0

ok, lapPt1, lapPt2 = vs.OverlapLineLine(begPt1, endPt1, begPt2, endPt2, tolerance)
vs.Message('OverlapLineLine returned: ' + str((ok, lapPt1, lapPt2)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
