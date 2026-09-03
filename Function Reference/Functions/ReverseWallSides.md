# ReverseWallSides

## Description
Switch the left and right side of a wall by reversing the direction of the wall.  This is an interface to the button with the same name on the Object Info palette.

```pascal
PROCEDURE ReverseWallSides(theWall : HANDLE);
```

```python
def vs.ReverseWallSides(theWall):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|Handle to the wall to operate on.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE ReverseWallSidesExample;
VAR
center_pt, start_pt, end_pt :VECTOR;
h :HANDLE;
BEGIN
center_pt.x := 0;
center_pt.y := 0;
start_pt.x := 100;
start_pt.y := 0;
end_pt.x := 0;
end_pt.y := 100;
RoundWall(center_pt.x, center_pt.y, start_pt.x, start_pt.y, end_pt.x, end_pt.y);
h := LNewObj;
ReverseWallSides(h);
END;
RUN(ReverseWallSidesExample);
```
#### Python ####
```python

```

```pascal
		pt3 := temp_pt;
	END;
	RoundWall(pt1.x, pt1.y, pt2.x, pt2.y, pt3.x, pt3.y);
	PolyPoints[I].h := LNewObj;
	IF PolyPoints[I].sweepAng > 0 THEN ReverseWallSides(PolyPoints[I].h);
END

		pt3 := temp_pt;
	END;
	RoundWall(pt1.x, pt1.y, pt2.x, pt2.y, pt3.x, pt3.y);
	PolyPoints[I].h := LNewObj;
	IF PolyPoints[I].sweepAng < 0 THEN ReverseWallSides(PolyPoints[I].h);
END;

		pt3     := temp_pt;
	END;
	RoundWall(pt1.x, pt1.y, pt2.x, pt2.y, pt3.x, pt3.y);
	walls[cnt].h := LNewObj;
	IF walls[cnt].sweepAng > 0 THEN ReverseWallSides(walls[cnt].h);
END;
```
```python
vs.ReverseWallSides(theWall)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
