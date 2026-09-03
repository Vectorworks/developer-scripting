# MoveTo

## Description
Sets the position of the graphics pen in the VectorWorks document using absolute coordinate values. The parameter specifies the X-Y coordinate location where the pen should be moved.

```pascal
PROCEDURE MoveTo(pX,pY : REAL);
```

```python
def vs.MoveTo(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|X-Y coordinate location.|

## Remarks
If you want to move a relative distance from the existing pen position, use Move.

## Examples
#### VectorScript ####
```pascal
MoveTo(4,3);
{moves the graphics pen to (4,3)}
```
#### Python ####
```python
vs.MoveTo(4, 3)
```

```pascal
BEGIN
	GetPolyPt(lineHandle, vertexNum, x, y);
	MoveTo(x, y);

BEGIN
	Absolute;
	MoveTo (x1, y1);
	LineTo (x2, y2);
END;

	OpenPoly;
	BeginPoly;
	LineTo ( x,  y);
END ELSE
	MoveTo (x, y);
```
```python
vs.MoveTo ( textPtx, textPty )
vs.DSelectAll()
vs.CreateText( vs.PSheet_No )
vs.SetFPat( vs.LNewObj(), 0 )
vs.Rotate( dTextRotation )

vs.SysBeep()
vs.Absolute()
vs.MoveTo( 0, 0 )
vs.BeginGroup()
vs.CreateText( message1 )
vs.SetTextVerticalAlign( vs.LNewObj(), 3 )
vs.SetTextJust( vs.LNewObj(), 2 )

if not vs.PShow_Joints:
	vs.PenSize( currPenSize )
	# Draw paving lines
	vs.MoveTo( p5 )
	vs.LineTo( p6 ); SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gPaving_Class)
	vs.MoveTo( p3 )
	vs.LineTo( p4 ); SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gPaving_Class)
	# Draw curb lines
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [05. Turn a Column Profile with Sweep](ai%20examples/05_SweepColumnAndTorus.md), [11. 2D Vector Math Toolkit](ai%20examples/11_VectorMathToolkit.md), [15. Uniform Arc-Length Resampling of a Polyline](ai%20examples/15_PolylineResampleUniform.md)

## See Also
VS Functions:
[Move](Move.md)

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
