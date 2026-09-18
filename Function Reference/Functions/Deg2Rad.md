# Deg2Rad

## Description
Function Deg2Rad converts the specified value (in degrees) to radians.

```pascal
FUNCTION Deg2Rad(degreeValue : REAL): REAL;
```

```python
def vs.Deg2Rad(degreeValue):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|degreeValue|REAL|Value in degrees.|

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
	alpha := alpha1;
	REPEAT
		alpha := alpha + 1 / incr;
		theta := Deg2Rad (alpha);
		m := (Sin (theta / 2) / theta) - (c / (2 * s));
		m := Str2Num (Num2Str (accuracy, m));
		IF m = 0 THEN
			a := alpha2

r := HPerim (ObjH) / Deg2Rad (theta2);
x := x0 + r * Cos (Deg2Rad (theta1));
y := y0 + r * Sin (Deg2Rad (theta1));
```
```python
offsetX = layerScale * ( kOrign_Constant * dUPI )
offsetX = offsetX * vs.Sin( vs.Deg2Rad ( dOffsetRotation ) )

def DrawParallelArcs( r1, sweep2D, distance, objClass ):
	theta = vs.Deg2Rad( sweep2D )
	a = r1 * vs.Tan( theta / 2 )
	b = a
	f = 0.0
	if theta > 0:

def DrawRoadway( r1, sweep2D, w ):
	theta = vs.Deg2Rad( sweep2D )
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
