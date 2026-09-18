# Sqrt

## Description
Function Sqrt returns the square root of the specified value.

```pascal
FUNCTION Sqrt(v : REAL): REAL;
```

```python
def vs.Sqrt(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Value for which to find the square root.|

## Remarks
Be aware that in VS, a number can be less than zero, even if it is equal to zero. The following script generates a "square root of a negative number" error...
```pascal
PROCEDURE GenerateError;
VAR
temp_r :REAL;
BEGIN
temp_r := -.00000000000000000000000000000000000001;
IF temp_r = 0 THEN Message(sqrt(temp_r));
END;
RUN(GenerateError);
```

## Examples
```pascal
BEGIN
	p := Sqrt (t * (2 * rtA - t));
	alpha := ArcSin ((rtA - t) / rtA);
	beta := (PI/2 - alpha) / 2;
	p1 := p - rtA * Tan (beta);
END ELSE

BEGIN
	a := 2 * r * Sin (Deg2Rad (alpha / 4));
	h := Sqrt (a^2 - (c / 2)^2);
	x0 := xc + (r - h) * Sin (Deg2Rad (beta));
	y0 := yc - (r - h) * Cos (Deg2Rad (beta));
	MoveTo (x0, y0);
	Relative;

BEGIN
	ColorDiff := Sqrt(Sqr(Abs(b2 - b1)) + Sqr(Distance(r1, g1, r2, g2)));
END;
```
```python
dx		= (p1[0] - p2[0]) / 2
dy		= (p1[1] - p2[1]) / 2
# Calc the distance from each point to the midpoint
dist	= vs.Sqrt(dx*dx + dy*dy)
if dist == 0:
	ok	= False
else:
	ok	= True
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
