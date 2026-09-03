# Tan

## Description
Function Tan returns the tangent of the specified value.

```pascal
FUNCTION Tan(v : REAL): REAL;
```

```python
def vs.Tan(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Angle, in radians.|

## Examples
```pascal
BEGIN
	p := Sqrt (t * (2 * rtA - t));
	alpha := ArcSin ((rtA - t) / rtA);
	beta := (PI/2 - alpha) / 2;
	p1 := p - rtA * Tan (beta);
END ELSE
	p1 := 0;

	theAngle     := Vec2Ang(ptA - centerPt);
	theArcLength := LenOfArc(centerPt, ptA, ptB);
	theta        := AngBVec(ptA-centerPt, ptB-centerPt);
	chord        := Sin(Deg2Rad(Abs(theta/2))) * theRadius * 2;
	T            := theRadius * Tan(Deg2Rad(theta/2));
END;

IF h = w THEN tanAlpha := 1
ELSE tanAlpha := Tan ( ArcTan ( (-2*Ixy) / (Ixx - Iyy) ) / 2 );
```
```python
def DrawParallelArcs( r1, sweep2D, distance, objClass ):
	theta = vs.Deg2Rad( sweep2D )
	a = r1 * vs.Tan( theta / 2 )
	b = a
	f = 0.0
	if theta > 0:
		f = ( distance + b * vs.Sin( theta ) - distance * vs.Cos( theta ) ) / vs.Sin( theta )

vs.BeginPoly()
vs.MoveTo( 0, 0 )
vs.MoveTo( w, 0 )
vs.ArcTo( w, r1 * vs.Tan( theta / 2 ), 0 )
vs.AddPoint( w + r1 - ( r1 * vs.Cos( theta ) ), r1 * vs.Sin( theta ) )
vs.MoveTo( -( r1 - ( r1 * vs.Cos( theta ) ) ), r1 * vs.Sin( theta ) )
vs.ArcTo( 0, r1 * vs.Tan( theta / 2 ), 0 )
vs.LineTo( 0, 0 )
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
