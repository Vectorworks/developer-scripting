# RoundWall

## Description
Procedure RoundWall creates a counter-clockwise round wall.

```pascal
PROCEDURE RoundWall(
				centerPtX,centerPtY : REAL;
				startPtX,startPtY   : REAL;
				endPtX,endPtY       : REAL);
```

```python
def vs.RoundWall(centerPt, startPt, endPt):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|centerPt|REAL|Center point of wall arc.|
|startPt|REAL|Start point of wall arc.|
|endPt|REAL|End point of wall arc.|

## Remarks
Creates a round wall the that is centered on the arc specified by the the three input points.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
x1, y1, x2, y2, x3, y3 :REAL;
lineHandle :HANDLE;
BEGIN
GetPt(x1, y1);
GetPtL(x1, y1, x2, y2);
MoveTo(x1, y1);
LineTo(x2, y2);
lineHandle := LNewObj;
GetPtL(x2, y2, x3, y3);
IF lineHandle <> NIL THEN DelObject(lineHandle);
RoundWall(x1, y1, x2, y2, x3, y3);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
		temp_pt := pt2;
		pt2 := pt3;
		pt3 := temp_pt;
	END;
	RoundWall(pt1.x, pt1.y, pt2.x, pt2.y, pt3.x, pt3.y);
	PolyPoints[I].h := LNewObj;
	IF PolyPoints[I].sweepAng > 0 THEN ReverseWallSides(PolyPoints[I].h);
END

	{swap beg and end point values}
	temp_v := Walls[1].beg_pt;Walls[1].beg_pt := Walls[1].END_pt;Walls[1].END_pt := temp_v;
END;
{create temp wall just to take the needed parameters}
RoundWall(Walls[1].center.x, Walls[1].center.y,
		Walls[1].beg_pt.x, Walls[1].beg_pt.y,
		Walls[1].END_pt.x, Walls[1].END_pt.y);
GetArcAll(LNewObj, temp_v, startAng, sweepAng, radius);
DelObject(LNewObj);
Walls[1].startAng := startAng;
Walls[1].sweepAng := sweepAng;

		temp_pt := pt2;
		pt2     := pt3;
		pt3     := temp_pt;
	END;
	RoundWall(pt1.x, pt1.y, pt2.x, pt2.y, pt3.x, pt3.y);
	walls[cnt].h := LNewObj;
	IF walls[cnt].sweepAng > 0 THEN ReverseWallSides(walls[cnt].h);
END;
```
```python
vs.RoundWall((0, 0), (0, 0), (0, 0))
```

## See Also
VS Functions:
[Wall](Wall.md)

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
