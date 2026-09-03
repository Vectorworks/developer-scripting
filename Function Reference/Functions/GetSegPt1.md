# GetSegPt1

## Description
Procedure GetSegPt1 returns the X-Y coordinates of the start point of the referenced line, wall, or linear dimension object.

```pascal
PROCEDURE GetSegPt1(
				h         : HANDLE;
				VAR pX,pY : REAL);
```

```python
def vs.GetSegPt1(h):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to line.|
|p|REAL|Coordinates of start point.|

## Examples
```pascal
BEGIN
	GetSegPt1(itemHandle, v1[1], v1[2]);
	GetSegPt2(itemHandle, v2[1], v2[2]);
	DrawLineLabel(v2 - v1, v1[1], v1[2]);
END;

if (wallH <> nil) & pSize_to_Wall_Length then BEGIN
	GetSegPt1(wallH, beg_pt.x, beg_pt.y);
	GetSegPt2(wallH, END_pt.x, END_pt.y);
	lngth := Distance(beg_pt.x, beg_pt.y, END_pt.x, END_pt.y);
	lngth := lngth + pAdd_to_Start + pAdd_to_END;
	beg_pt := WorldToObjectCoords(pluginH, beg_pt);

BEGIN
	GetSegPt1(gWallHand, begwall_pt.x, begwall_pt.y);
	GetSegPt2(gWallHand, endwall_pt.x, endwall_pt.y);
```
```python
import vs

# Procedure GetSegPt1 returns the X-Y coordinates of the start point of the
# referenced line, wall, or linear dimension object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetSegPt1(h)
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
