# Sin

## Description
Function Sin returns the sine of the specified value. The base value is assumed to represent an angle in radians.

```pascal
FUNCTION Sin(v : REAL): REAL;
```

```python
def vs.Sin(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Numeric value for which to find the sine.|

## Examples
```pascal
	theRadius    := Norm(ptA - centerPt);
	theAngle     := Vec2Ang(ptA - centerPt);
	theArcLength := LenOfArc(centerPt, ptA, ptB);
	theta        := AngBVec(ptA-centerPt, ptB-centerPt);
	chord        := Sin(Deg2Rad(Abs(theta/2))) * theRadius * 2;
	T            := theRadius * Tan(Deg2Rad(theta/2));
END;

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

if theta > 0:
	f = ( distance + b * vs.Sin( theta ) - distance * vs.Cos( theta ) ) / vs.Sin( theta )

vs.MoveTo( 0, 0 )
vs.MoveTo( w, 0 )
vs.ArcTo( w, r1 * vs.Tan( theta / 2 ), 0 )
vs.AddPoint( w + r1 - ( r1 * vs.Cos( theta ) ), r1 * vs.Sin( theta ) )
vs.MoveTo( -( r1 - ( r1 * vs.Cos( theta ) ) ), r1 * vs.Sin( theta ) )
vs.ArcTo( 0, r1 * vs.Tan( theta / 2 ), 0 )
vs.LineTo( 0, 0 )
vs.EndPoly()
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
