# CircleCircleInters

## Description
Finds the intersection of two circles.

```pascal
FUNCTION CircleCircleInters(
				cenPt1  : VECTOR;
				cenPt2  : VECTOR;
				radius1 : REAL;
				radius2 : REAL;
				VAR pt1 : VECTOR;
				VAR pt2 : VECTOR): BOOLEAN;
```

```python
def vs.CircleCircleInters(cenPt1, cenPt2, radius1, radius2):
    return (BOOLEAN, pt1, pt2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|cenPt1|VECTOR|   |
|cenPt2|VECTOR|   |
|radius1|REAL|   |
|radius2|REAL|   |
|pt1|VECTOR|   |
|pt2|VECTOR|   |

## Examples
```pascal
if not isChordBearSelected   then BEGIN
	begPt.x := verts[currentVert, 1];
	begPt.y := verts[currentVert, 2];
	cenPt := begPt + Ang2Vec(backTangent - 90, radius);
	boo := CircleCircleInters(begPt, cenPt, chordDist, radius, pt1, pt2);
	num1 := Norm(pt1 - begPt);
	num2 := Norm(pt2 - begPt);
	IF num1 > num2
		THEN endPt := pt1

BEGIN
	{get the point on the pitch circle of sprocket #2 (vector 6)}
	OK := CircleCircleInters (v4, v3, pitch, r2, v5, v6);
	beta1 := Vec2Ang (v6 - v4);
	totalNumLinks := totalNumLinks + 1;
```
```python
import vs

# Finds the intersection of two circles.
cenPt1 = (0, 0)
cenPt2 = (1, 1)
radius1 = 1.0
radius2 = 1.0

ok, pt1, pt2 = vs.CircleCircleInters(cenPt1, cenPt2, radius1, radius2)
vs.Message('CircleCircleInters returned: ' + str((ok, pt1, pt2)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
