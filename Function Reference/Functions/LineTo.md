# LineTo

## Description
Procedure LineTo creates a line object in the document. LineTo draws from the current graphics pen position to the specified coordinate location. The line object is drawn with the current default attributes unless otherwise specified in the VectorScript routine.

```pascal
PROCEDURE LineTo(pX,pY : REAL);
```

```python
def vs.LineTo(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Line endpoint.|

## Remarks
(Joel Sciamma, 2006.08.14): After the line is drawn, the graphics pen is set to the end of the line ready to draw another object. Use [ MoveTo](MoveTo.md) to reset the graphics pen position.

## Examples
#### VectorScript ####
```pascal
LineTo(3,4);
{draws a line from the current pen position to (3, 4)}
```
#### Python ####
```python

```

```pascal
BEGIN
	IF r[i] > 0 THEN
		ArcTo(x0 + x[i],y0 + y[i],r[i])
	ELSE
		LineTo(x0 + x[i], y0 + y[i]);
END;

BEGIN
	BeginGroup;
		MoveTo(pt1[1], pt1[2]);
		LineTo(theIntersection[1], theIntersection[2]);
		LineTo(pt2[1], pt2[2]);
	EndGroup;
END;

BEGIN
	Absolute;
	MoveTo (x1, y1);
	LineTo (x2, y2);
END;
```
```python
vs.BeginPoly()
vs.MoveTo( -0.5 * dMmarkerSize, 0.5 * dMmarkerSize )
vs.ArcTo( 	0,1 * dMmarkerSize, 0 )
vs.LineTo( 	0.5 * dMmarkerSize, 0.5 * dMmarkerSize )
vs.LineTo( 	0,1 * dMmarkerSize )
vs.EndPoly()
vs.MoveTo ( 0,1.5 	* dMmarkerSize )

vs.MoveTo( 0, 0 )
vs.MoveTo( -distance, 0 )
vs.ArcTo( 0, e, r2 )
vs.LineTo( f * vs.Sin( theta ), f * vs.Cos( theta ) )
vs.MoveTo( distance * vs.Cos( theta ), -distance * vs.Sin( theta ) )
vs.ArcTo( -b * vs.Sin( theta ), -b * vs.Cos( theta ), r1 )
vs.LineTo( 0, -a )
vs.MoveTo( 0, 0 )

vs.PenSize( currPenSize )
# Draw paving lines
vs.MoveTo( p5 )
vs.LineTo( p6 ); SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gPaving_Class)
vs.MoveTo( p3 )
vs.LineTo( p4 ); SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gPaving_Class)
# Draw curb lines
vs.LineTo( p3 ); SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gCurb_Class)
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [05. Turn a Column Profile with Sweep](ai%20examples/05_SweepColumnAndTorus.md), [11. 2D Vector Math Toolkit](ai%20examples/11_VectorMathToolkit.md), [15. Uniform Arc-Length Resampling of a Polyline](ai%20examples/15_PolylineResampleUniform.md)

## See Also
VS Functions: [Absolute](Absolute.md) | [Relative](Relative.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
