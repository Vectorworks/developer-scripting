# SetArc

## Description
Procedure SetArc sets the start and sweep angles of the referenced arc or round wall object.   Specify the angles in degrees.

```pascal
PROCEDURE SetArc(
				h          : HANDLE;
				startAngle : REAL;
				arcAngle   : REAL);
```

```python
def vs.SetArc(h, startAngle, arcAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to arc.|
|startAngle|REAL|New start angle of arc.|
|arcAngle|REAL|New sweep angle of arc.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetArcSetArcExample;
VAR
h :HANDLE;
startAng, sweepAng :REAL;
BEGIN
h := FSActLayer;
GetArc(h, startAng, sweepAng);
SetArc(h, startAng, sweepAng + 10);
END;
RUN(GetArcSetArcExample);
```
#### Python ####
```python

```

```pascal
6: BEGIN	{ Arc/Circle }
	getArc(hTemp, startA, endA);
	setArc(hTemp, 0.0, 360.0);
	getbbox(hTemp, x1, y1, x2, y2);
	setbbox(hTemp, x1*factor, y1*factor, x2*factor, y2*factor);
	setArc(htemp, startA, endA);
	END;

					PolyPoints[I].h := oldWalls[found].h;
					oldWalls[found].WasUsed := TRUE;
				END;{ else if fullyTheSameWall = 0 then begin
					temp_pt := walls[1].center - oldWalls[found].center;
					SetArc(oldWalls[found].h, walls[1].startAng, walls[1].sweepAng);
					{! Need the ability to set the radius of a round wall.}
					{HMove(oldwalls[found].h, temp_pt.x, temp_pt.y);}
{				END;}

BEGIN
	HCenter(h, cen_pt.x, cen_pt.y);
	SetArc (h, startAng, sweepAng);
	{! IF GetType(h) = 6 THEN  ELSE}
	IF IsArcBasedWall(h) THEN SetObjectVariableReal(h, 571, radius);
END;
```
```python
vs.SetArc(h, 1.0, 2.0)
```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
