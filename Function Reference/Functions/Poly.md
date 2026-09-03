# Poly

## Description
Procedure Poly creates a polygon object in the document. Vertices of the polygon are specified by a parameter list of x1,y1 through xn,yn, which correspond to the coordinate locations of each vertex.

```pascal
PROCEDURE Poly(p : REAL);
```

```python
def vs.Poly(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|   |

## Examples
#### VectorScript ####
```pascal
Poly(0,0,-0.5,1,0.5,1.5,2,1,1,-0.5);
```
#### Python ####
```python
vs.Poly(0,0,-0.5,1,0.5,1.5,2,1,1,-0.5)

# Or using a list:
points = [0,0,-0.5,1,0.5,1.5,2,1,1,-0.5]
vs.Poly(*points)
```

```pascal
IF sBlind = kBCStrLeft THEN
	IF pEnd_Finish = kBCStrPenLeft THEN
		IF bShowDetail THEN BEGIN
			Poly(
				X,Y,
				X,Y+Length,
				X+Depth+Overhang,Y+Length,
				X+Depth+Overhang, Y -Depth + Overhang,
				X+Depth, Y -Depth + Overhang,
				X+Depth, Y, X,Y
			);

BEGIN
BeginXtrd(Z,CabHeight);
	Poly(X-CabThick, Y-CabThick,
	X-LeftCabLength+CabThick, Y-CabThick,
	X-LeftCabLength+CabThick, Y-CabDepth+FaceThick,
	X-CabDepth+FaceThick, Y-CabDepth+FaceThick,
	X-CabDepth+FaceThick, Y-CabLength+CabThick,
	X-CabThick, Y-CabLength+CabThick);
EndXtrd;

SetZVals(cHeight,cRoof_Thickness);
BeginRoof(-cWidth/2,cWidth/2,0.00,cWidth/2,-cWidth/4,cWidth/4,cRise,cWidth/2,1,0);
Move3D(0.0,0.0,cHeight);
	ClosePoly;
	Poly(
	-(cWidth/2+cOverhang),(cWidth/2+cOverhang),
	0.0,0.0,
	-(cWidth/2+cOverhang),0.0
	);
	EndGroup;
	SetFPat(lNewObj,1);
	SetObjExpandTexture(lNewObj,FALSE);
```
```python
import vs

# Procedure Poly creates a polygon object in the document.
p = 1.0

vs.Poly(p)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
