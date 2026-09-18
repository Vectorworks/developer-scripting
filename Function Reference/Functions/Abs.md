# Abs

## Description
Function Abs returns the absolute value of the specified value.

```pascal
FUNCTION Abs(v : REAL): REAL;
```

```python
def vs.Abs(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Real number.|

## Examples
```pascal
	theRadius    := Norm(ptA - centerPt);
	theAngle     := Vec2Ang(ptA - centerPt);
	theArcLength := LenOfArc(centerPt, ptA, ptB);
	theta        := AngBVec(ptA-centerPt, ptB-centerPt);
	chord        := Sin(Deg2Rad(Abs(theta/2))) * theRadius * 2;
	T            := theRadius * Tan(Deg2Rad(theta/2));
END;

BEGIN
	EqAng := (Abs(ConvertTo360Ang(ang1) - ConvertTo360Ang(ang2)) < fuzz);
END;

BEGIN
	Offset := ABS(Sin(kTaper)*RailThick);
	IF TTap THEN
		BEGIN
		Y2 := Y1-Offset;
		END
```
```python
if vs.Abs(pt2[1]) > vs.Abs( pt1[1] ):
	pt1 = ( pt1[0], vs.Abs( pt2[1] ) )
else:
	pt1 = ( pt1[0], vs.Abs( pt1[1] ) )

# Draw roadway
if ( vs.Abs( vs.PRise ) < kMinDrop ):
	vs.BeginFloor( thickness )
	DrawRoadway( r1, sweep2D, w )
else:
	vs.SetZVals( 0, thickness )
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
