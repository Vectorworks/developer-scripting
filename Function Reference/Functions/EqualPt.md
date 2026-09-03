# EqualPt

## Description
Function EqualPt returns whether the two specified coordinate locations are equal (i.e., the same point, to 12 significant digits).

```pascal
FUNCTION EqualPt(
				p1X,p1Y : REAL;
				p2X,p2Y : REAL): BOOLEAN;
```

```python
def vs.EqualPt(p1, p2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Coordinates of first comparison point.|
|p2|REAL|Coordinates of second comparison point.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
x1, y1, x2, y2 :REAL;
BEGIN
x1 := 1;
y1 := 1;
x2 := 1.0000000000001;
y2 := 1.0000000000001;
Message(EqualPt(x1, y1, x2, y2));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	x1 = 1
	y1 = 1
	x2 = 1.0000000000001
	y2 = 1.0000000000001
	vs.Message(vs.EqualPt(x1, y1, x2, y2))
Example()
```

```pascal
{ there is a line section from the last arc to this arc we need to fill ... }
IF (GetVertexType(lineHandle, v0) = kArcType) AND (NOT EqualPt(p2[1], p2[2], gLastP3[1], gLastP3[2])) then
BEGIN
	HandleLine(gLastP3, p2);
END;

	isCircle := EqualPt (x1, y1, x2, y2);
END

	theArea := TriArea(p2[1],p2[2],p3[1],p3[2],theCenter[1],theCenter[2]);
	IF (theArea > 0) THEN sign := 1 ELSE sign := -1;
	IF (sign = 1) THEN clockmode := kCounterwise ELSE clockmode := kClockwise;
{there is a line section from the last arc to this arc we need to fill ... }
	IF (GetVertexType(lineHandle,v0) = 3) AND (NOT EqualPt(p2[1],p2[2],gLastP3[1],gLastP3[2])) THEN HandleLine(gLastP3,p2,FALSE);
{there is a line on this curve segment before the pt of curvature, lets draw our station pts along it }
	pt := startVert;
	IF (GetVertexType(lineHandle,v0) <> 3) AND (NOT EqualPt(pt[1],pt[2],p2[1],p2[2])) THEN HandleLine(startVert,p2,FALSE);
```
```python
import vs

# , the same point, to 12 significant digits).
p1 = (0, 0)
p2 = (2, 2)

ok = vs.EqualPt(p1, p2)
if ok:
    vs.Message('EqualPt succeeded')
else:
    vs.Message('EqualPt failed')
```

## See Also
VS Functions:
* [EqPt](EqPt.md)
* [EqPt2D](EqPt2D.md)
* [EqPt3D](EqPt3D.md)

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
