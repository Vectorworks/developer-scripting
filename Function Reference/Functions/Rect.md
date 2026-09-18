# Rect

## Description
Procedure Rect creates a rectangle object in a VectorWorks document.

The procedure will accept coordinate definitions by either of two methods : coordinate values or distance angle values. Coordinate values are the absolute coordinate locations(in the documents' coordinate system) and are expressed as x and y values. 

Distance-angle values are expressed as a distance and angle from the current pen position. For Rect, two distance angle pairs are required to specify the top left and bottom right of the rectangle object.

```pascal
PROCEDURE Rect(
				p1x : REAL;
				p1y : REAL;
				p2x : REAL;
				p2y : REAL);
```

```python
def vs.Rect(p1x, p1y, p2x, p2y):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1x|REAL|Top left X coordinate of rectangle.|
|p1y|REAL|Top left Y coordinate of rectangle.|
|p2x|REAL|Bottom right X coordinate of rectangle.|
|p2y|REAL|Bottom right Y coordinate of rectangle.|

## Remarks
*\_c\_* (2016.03.28): An example using distance-angle. Don't forget to use the pound notation (#):
```pascal
MoveTo(10m, 20m); { set pen position at x, y: 10m, 20m }
Rect(1m, #0, 2m, #90); 
{ draws from the current pen position 
an unrotated rectangle with width = 1m and height = 2m }
```

## Examples
[SelectandDelObjects](examples/SelectandDelObjects.md)

```pascal
		IF IsLineStyleByClass THEN SetLSByClass( LNewObj );
	END
ELSE IF EndFinish = kBCStrEndNone THEN BEGIN
	IF bShowDetail THEN BEGIN
		Rect(xOrg,yOrg,Length,Depth);
		SetLW(LNewObj,kThinLine);
		IF IsLineStyleByClass THEN SetLSByClass( LNewObj );
		HMoveBackward(LNewObj, TRUE);
		MoveTo(XOrg,Depth);

BEGIN
	Rect(originX, originY, originX + lngth, originY + thickness);
	SetFPat(LNewObj, 1);
	SetLSN(LNewObj, 0);
END

BEGIN
	IF SLength < 0 THEN {Utility Cabinet}
		Rect(X1-kSlatSpace-I*SlatWidth,Y1,X1+kSlatSpace-I*SlatWidth,Y1-SHeight)
	ELSE {Other cabinets}
		Rect(X1-kSlatSpace+I*SlatWidth,Y1,X1+kSlatSpace+I*SlatWidth,Y1-SHeight);
END;
```
```python
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 0 )
b1, b2 = vs.GetBBox( vs.LNewObj() )
vs.Rect( kBf * b1[0], kBf * b1[1], kBf * b2[0], kBf * b2[1] )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 1 )
vs.HMoveBackward( vs.LNewObj(), False )
vs.EndGroup()
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md), [06. Boolean Solids: Drill a Hole Through a Block](ai%20examples/06_BooleanSolids.md), [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md)

## See Also
VS Functions:
[RRect](RRect.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
