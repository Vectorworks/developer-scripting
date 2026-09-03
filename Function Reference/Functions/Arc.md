# Arc

## Description
Procedure Arc creates an arc object, or a polyline object, in the active document. If p1 and p2 define a perfect square, an arc will be created, with its center point at the center of the square. If p1 and p2 define a rectangle, a polyline will be created which will represent the oval segment defined by the rectangle.

```pascal
PROCEDURE Arc(
				p1X,p1Y    : REAL;
				p2X,p2Y    : REAL;
				StartAngle : REAL;
				ArcAngle   : REAL);
```

```python
def vs.Arc(p1, p2, StartAngle, ArcAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Top left coordinate of bounding box of oval defining the arc.|
|p2|REAL|Bottom right coordinate of bounding box of oval defining the arc.|
|StartAngle|REAL|Start angle of drawn arc.|
|ArcAngle|REAL|Sweep angle of drawn arc.|

## Remarks
The bounding box of the arc or polyline is not the same as the bounding box returned by GetBBox -- unless the sweep angle of the arc is 360 degrees.

## Examples
#### VectorScript ####
```pascal
Arc(0,0,2,2,#45,#90);
{draws an 90 degree arc with a start angle of 45 degrees}
```
#### Python ####
```python
vs.Arc(0,0,2,2,45,90)
```

```pascal
	x0 := xc + (r - h) * Sin (Deg2Rad (beta));
	y0 := yc - (r - h) * Cos (Deg2Rad (beta));
	MoveTo (x0, y0);
	Relative;
	Arc (-r, r, r, -r, (90 - alpha/2 + beta), alpha);
END;

MoveTo(CenterX-Length-(Radius*Sin(theta)),CenterY-Length-(Radius*Cos(Theta)));
LineTo(CenterX-Length-(Radius*Cos(Theta)),CenterY-Length-(Radius*Sin(Theta)));
SetLW(LNewObj,kThinLine);
SetLSN(LNewObj,gDashedLine);
Arc(X+inset-Length,Y+inset-Length,X-inset,Y-inset,270-dTheta,270+2*dTheta);
SetLW(LNewObj,kThinLine);
SetLSN(LNewObj,gDashedLine);
DSelectAll;

IF GetPref(16) THEN	{black background}
	SetPenFore(lnewobj,0,0,0)
ELSE SetPenFore(lnewobj,65535,65535,65535);
IF pFlip
	THEN Arc(0.0,pLineLength/2,pLineLength,-pLineLength/2,190,160.0)
	ELSE Arc(0.0,pLineLength/2,pLineLength,-pLineLength/2,170,-160.0);
```
```python
import vs

# Procedure Arc creates an arc object, or a polyline object, in the active
# document.
p1 = (0, 0)
p2 = (2, 2)
StartAngle = 45.0
ArcAngle = 90.0

vs.Arc(p1, p2, StartAngle, ArcAngle)
newObj = vs.LNewObj()  # handle to the newly created object
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
