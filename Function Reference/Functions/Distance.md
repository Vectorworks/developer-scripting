# Distance

## Description
Function Distance returns the distance between the two specified coordinate locations.

```pascal
FUNCTION Distance(
				x1 : REAL;
				y1 : REAL;
				x2 : REAL;
				y2 : REAL): REAL;
```

```python
def vs.Distance(x1, y1, x2, y2):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x1|REAL|X coordinate of first point.|
|y1|REAL|Y coordinate of first point.|
|x2|REAL|X coordinate of second point.|
|y2|REAL|Y coordinate of second point.|

## Examples
#### VectorScript ####
```pascal
d:=Distance(0,2,4,5);
{returns the distance between (0,2) and (4,5)}
```
#### Python ####
```python
d= vs.Distance(0,2,4,5)
```

```pascal
BEGIN
	GetLine (x1, y1, x2, y2);
	c := Distance (x1, y1, x2, y2);
	IF c >= s THEN
	BEGIN
		isLine := TRUE;
		c := s;

BEGIN
	doorLength := Distance(gLeftLength,gDepth,gDepth,gLength)-2*gSideReveal;
	ChangeToClass(gHiddenClass);
	Draw3DDiagCornerCarcus(0,0,0,gDepth,gLength,gLeftLength,gHeight,gKickInset,gKickHeight ,gCabThick,gFaceThick,FALSE);
	BeginGroup;
	ChangeToClass(gHiddenClass);

if (wallH <> nil) & pSize_to_Wall_Length then BEGIN
	GetSegPt1(wallH, beg_pt.x, beg_pt.y);
	GetSegPt2(wallH, END_pt.x, END_pt.y);
	lngth := Distance(beg_pt.x, beg_pt.y, END_pt.x, END_pt.y);
	lngth := lngth + pAdd_to_Start + pAdd_to_END;
	beg_pt := WorldToObjectCoords(pluginH, beg_pt);
	originX := beg_pt.x - pAdd_TO_Start;
	originY := beg_pt.y + offset - (WallWidth(wallH) / 2);
```
```python
import vs

# Function Distance returns the distance between the two specified coordinate
# locations.
x1 = 0.0
y1 = 0.0
x2 = 2.0
y2 = 1.0

distance = vs.Distance(x1, y1, x2, y2)
vs.Message('Distance returned: ' + str(distance))
```

## See Also
VS Functions:
[Norm](Norm.md)

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
