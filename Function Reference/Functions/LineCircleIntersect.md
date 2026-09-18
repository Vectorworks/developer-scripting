# LineCircleIntersect

## Description
Finds the intersection points of a line and a circle.

```pascal
FUNCTION LineCircleIntersect(
				begPt   : VECTOR;
				endPt   : VECTOR;
				cenPt   : VECTOR;
				radius  : REAL;
				VAR pt1 : VECTOR;
				VAR pt2 : VECTOR): BOOLEAN;
```

```python
def vs.LineCircleIntersect(begPt, endPt, cenPt, radius):
    return (BOOLEAN, pt1, pt2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|begPt|VECTOR|   |
|endPt|VECTOR|   |
|cenPt|VECTOR|   |
|radius|REAL|   |
|pt1|VECTOR|   |
|pt2|VECTOR|   |

## Remarks
In VS Python, this function returns 3-element tuples with gibberish in the third element regardless whether you give it 2- or 3-element tuples.
This function checks and returns the intersection of the circle with an infinite line defined by the two supplied points.

## Examples
```pascal
if not ValidBearingStr(tmpStr, chordBear) THEN ok := false ELSE BEGIN
	begPt.x := verts[currentVert, 1];
	begPt.y := verts[currentVert, 2];
	cenPt := begPt + Ang2Vec(backTangent - 90, radius);
	boo := LineCircleIntersect(begPt, begPt + Ang2Vec(chordBear, 1), cenPt, radius, pt1, pt2);
	num1 := Norm(pt1 - begPt);
	num2 := Norm(pt2 - begPt);
	IF num1 > num2
		THEN endPt := pt1

BEGIN
	pt1.z := 0; pt2.z := 0;
	IF LineCircleIntersect(beg_pt, end_pt, cen_pt, rad, pt1, pt2) THEN BEGIN
		IF PtOnArc(pt1, cen_pt, rad, startAng, sweepAng, fuzz) THEN pt1.z := 1;
		IF PtOnArc(pt2, cen_pt, rad, startAng, sweepAng, fuzz) THEN pt2.z := 1;
	END;

beg_pt := verts[before].pt;
END_pt := verts[temp1].pt;
cen_pt := verts[after].center;
rad    := verts[after].offset;
IF LineCircleIntersect(beg_pt, end_pt, cen_pt, rad, pt1, pt2) THEN BEGIN
	IF Dist(pt1, dur_pt) < Dist(pt2, dur_pt)
		THEN inters_pt := pt1
		ELSE inters_pt := pt2;
END;
```
```python
import vs

# Finds the intersection points of a line and a circle.
begPt = (0, 0)
endPt = (2, 2)
cenPt = (2, 0)
radius = 1.0

ok, pt1, pt2 = vs.LineCircleIntersect(begPt, endPt, cenPt, radius)
vs.Message('LineCircleIntersect returned: ' + str((ok, pt1, pt2)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
