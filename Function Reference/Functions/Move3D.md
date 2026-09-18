# Move3D

## Description
Procedure Move3D moves the most recently created three-dimensional object a relative distance from it's original location. The object is moved relative to its center.

```pascal
PROCEDURE Move3D(
				xDistance : REAL;
				yDistance : REAL;
				zDistance : REAL);
```

```python
def vs.Move3D(xDistance, yDistance, zDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xDistance|REAL|X offset distance.|
|yDistance|REAL|Y offset distance.|
|zDistance|REAL|Z offset ditance.|

## Examples
#### VectorScript ####
```pascal
BeginXtrd(0',2&quot;);
Rect(0&quot;,1&quot;,1&quot;,0&quot;);
EndXtrd;
Move3D(3&quot;,1&quot;,2&quot;);
```
#### Python ####
```python

```

```pascal
EndPoly;
SetPolyClosed(lNewObj,TRUE);
EndXtrd;
SET3DRot(LNewObj,90,0,0,X,Y-KickInset-CabThick,Z+KickInset);
Move3D(0, 0, CabLength -2*KickInset -CabThick);

SetZVals(cHeight,cRoof_Thickness);
BeginRoof(-cWidth/2,cWidth/2,0.00,cWidth/2,-cWidth/4,cWidth/4,cRise,cWidth/2,1,0);
Move3D(0.0,0.0,cHeight);
	ClosePoly;
	Poly(
	-(cWidth/2+cOverhang),(cWidth/2+cOverhang),
	0.0,0.0,

	);
EndXtrd;
ResetOrientation3D;
Rotate3D(#0.0,#0.0,#0.0);
Move3D(0e0',0e0',0e0');
BeginXtrd(-7.1875e-1',7.1875e-1');
	Poly(
	-1.35688e0',1.5625e0',
	-4.61047e-1',1.4375e0',
```
```python
if drop > 0:
	vs.BeginRoof( 0, 0, w, 0, r1 + w / 2, gutterBottomY, -drop, r1, 2, thickness )
	DrawRoadway( r1, sweep2D, w )
	vs.Move3D( 0, 0, drop )
```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
