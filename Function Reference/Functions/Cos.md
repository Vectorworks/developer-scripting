# Cos

## Description
Function Cos returns the cosine of the specified value. The base value is assumed to represent an angle in radians.

```pascal
FUNCTION Cos(v : REAL): REAL;
```

```python
def vs.Cos(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|The angle for which to find the cosine.|

## Examples
```pascal
xc := x1 + c * Cos (Deg2Rad (beta)) / 2;
yc := y1 + c * Sin (Deg2Rad (beta)) / 2;
x2 := x1 + c * Cos (Deg2Rad (beta));
y2 := y1 + c * Sin (Deg2Rad (beta));

r := HPerim (ObjH) / Deg2Rad (theta2);
x := x0 + r * Cos (Deg2Rad (theta1));
y := y0 + r * Sin (Deg2Rad (theta1));

ChangeToClass(gHiddenClass);
IF (Length<=2*Depth) AND NOT(pUneven) THEN BEGIN
	MoveTo(CenterX-Length-(Radius*Sin(theta)),CenterY-Length-(Radius*Cos(Theta)));
	LineTo(CenterX-Length-(Radius*Cos(Theta)),CenterY-Length-(Radius*Sin(Theta)));
	SetLW(LNewObj,kThinLine);
	SetLSN(LNewObj,gDashedLine);
	Arc(X+inset-Length,Y+inset-Length,X-inset,Y-inset,270-dTheta,270+2*dTheta);
```
```python
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
