# PtInRect

## Description
Function PtInRect returns whether the coordinate location is located within the specified rectangular boundary.

```pascal
FUNCTION PtInRect(
				pointX,pointY : REAL;
				rect1X,rect1Y : REAL;
				rect2X,rect2Y : REAL): BOOLEAN;
```

```python
def vs.PtInRect(point, rect1, rect2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|point|REAL|X-Y coordinate point location.|
|rect1|REAL|Top left coordinate of rectangular area.|
|rect2|REAL|Bottom right coordinate of rectangular area.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
pointX, pointY, rect1X, rect1Y, rect2X, rect2Y :REAL;
BEGIN
pointX := 1;
pointY := 1;
rect1X := 0;
rect1Y := 2;
rect2X := 2;
rect2Y := 0;
Message(PtInRect(pointX, pointY, rect1X, rect1Y, rect2X, rect2Y));
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
temp_h := FInGroup(target);
while temp_h <> nil do BEGIN
	if GetName(GetRecord(temp_h, NumRecords(temp_h))) = 'Flowchart Node' then BEGIN
		GetBBox(temp_h, p1x, p1y, p2x, p2y);
		if PtInRect(pt.x, pt.y, p1x, p1y, p2x, p2y) then BEGIN
			target := temp_h;
			temp_h := NIL;
		END;

	pt3.y := bottom;
	pt4.x := left;
	pt4.y := bottom;
	PtInOrOnRect :=
		PtInRect(x, y, left, top, right, bottom) |
		PtOnLine(test_pt, pt1, pt2, fuzz) |
		PtOnLine(test_pt, pt2, pt3, fuzz) |
		PtOnLine(test_pt, pt3, pt4, fuzz) |
		PtOnLine(test_pt, pt4, pt1, fuzz);
END;

{ ExistCLineMid_Pt is within the top half of the photo bbox }
IF PtInRect	(
			ExistCLineMid_Pt.x, ExistCLineMid_Pt.y,
			PhotoObjTopL_Pt.x, PhotoObjTopL_Pt.y,
			PhotoObjBotR_Pt.x, PhotoObjCtr_Pt.y
			)
THEN NewCLineStart_Pt.y := ( PhotoObjBotR_Pt.y + PhotoObjCtr_Pt.y ) / 2	{ Y location in the middle of the bottom half }
ELSE NewCLineStart_Pt.y := ( PhotoObjTopL_Pt.y + PhotoObjCtr_Pt.y ) / 2;{ Y location in the middle of the top half }
```
```python
result = vs.PtInRect((0, 0), rect1, rect2)
```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
