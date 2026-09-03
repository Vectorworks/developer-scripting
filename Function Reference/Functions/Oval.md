# Oval

## Description
Procedure Oval creates an oval object in a VectorWorks document.

```pascal
PROCEDURE Oval(
				p1X,p1Y : REAL;
				p2X,p2Y : REAL);
```

```python
def vs.Oval(p1, p2):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Top left coordinate of oval bounding box.|
|p2|REAL|Bottom right coordinate of oval bounding box.|

## Examples
```pascal
pushattrs;
fillpat(1);
fillback(65535,42000,0);
BeginMXtrd(0.0,cWidth/3);
	Oval(-cWidth/6,-cWidth/6,cWidth/6,cWidth/6);
	Oval(-cWidth/6,-cWidth/6,cWidth/6,cWidth/6);
	Oval(-cWidth/9,-cWidth/9,cWidth/9,cWidth/9);
	Oval(-cWidth/10,-cWidth/10,cWidth/10,cWidth/10);
	Oval(-cWidth/12,-cWidth/12,cWidth/12,cWidth/12);

BEGIN
	IF gStructShape = kRectangularC THEN
		RRect(-width/2, depth/2, width/2, -depth/2, 2*radius, 2*radius)
	ELSE Oval(-width/2, depth/2, width/2, -depth/2);
END

IF pConfig=kDLSConfig1 THEN Oval(-SizeFactor,-SizeFactor/2,0,SizeFactor/2)
ELSE IF pConfig=kDLSConfig3 THEN Rect(-SizeFactor,-SizeFactor/2,0,SizeFactor/2)
ELSE IF pConfig=kDLSConfig2 THEN BEGIN
	SetRadius;
	RRect(-SizeFactor,-SizeFactor/2,0,SizeFactor/2,rad,rad);
	END;
```
```python
# Draw Oval
vs.Absolute()
vs.FillPat(0)
vs.Oval( -dMmarkerSize * 0.7075, dMmarkerSize * 0.7075, dMmarkerSize * 0.7075, -dMmarkerSize * 0.7075 )
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md), [06. Boolean Solids: Drill a Hole Through a Block](ai%20examples/06_BooleanSolids.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
