# SetSegPt2

## Description
Procedure SetSegPt2 sets the location of the end point of the referenced line or wall object.

```pascal
PROCEDURE SetSegPt2(
				h     : HANDLE;
				pX,pY : REAL);
```

```python
def vs.SetSegPt2(h, p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to arc.|
|p|REAL|New end point of line.|

## Remarks
Although GetSegPt1 works on linear dimensions this call does not successfully set the pt for a dimension.

## Examples
```pascal
BEGIN
	Absolute;
	IF getIntersect2 (h1, hL, xt, yt) THEN
		SetSegPt2 (h1, xt, yt);
	Relative;
END;

2: BEGIN	{ Line }
	getsegpt1(hTemp, x1, y1);
	getsegpt2(hTemp, x2, y2);
	setsegpt1(hTemp, x1*factor, y1*factor);
	setsegpt2(hTemp, x2*factor, y2*factor);
	END;

{Now reshape the existing straight wall, or draw a new one.}
if found > 0 then BEGIN
	oldWalls[found].WasUsed := TRUE;
	SetSegPt2(oldWalls[found].h, walls[1].beg_pt.x, walls[1].beg_pt.y);
	SetSegPt1(oldWalls[found].h, walls[1].END_pt.x, walls[1].END_pt.y);
	PolyPoints[I].h := oldWalls[found].h;
```
```python
import vs

# Procedure SetSegPt2 sets the location of the end point of the referenced
# line or wall object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
p = (0, 0)

vs.SetSegPt2(h, p)
```

## See Also
VS Functions:
[SetSegPt1](SetSegPt1.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
