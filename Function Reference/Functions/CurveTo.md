# CurveTo

## Description
Procedure CurveTo creates a bezier vertex point at the specified point. Parameter p specifies the coordinate location of the vertex.

```pascal
PROCEDURE CurveTo(pX,pY : REAL);
```

```python
def vs.CurveTo(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinate of vertex.|

## Examples
```pascal
BEGIN
	AngleVar;
	CASE vertexTypeFlag OF
		0 : LineTo (vertexX, #vertexY);
		1 : CurveTo (vertexX, #vertexY);
		2 : CurveThrough (vertexX, #vertexY);
		3 : ArcTo (vertexX, #vertexY, 0);
	END;

Absolute;
ClosePoly;
BeginPoly;
	LineTo(x1,0);
	CurveTo(x1,k1*y2);
	CurveTo(k2*x1,k2*y2);
	CurveTo(k1*x1,y2);
	CurveTo(k1*x2,y2);
	CurveTo(k2*x2,k2*y2);

IF ((i = start_i) & skip)
	THEN moveto(x, y)
	ELSE CASE t OF
		0: AddPoint(x, y);		{point}
		1: CurveTo(x, y);		{bezier}
		2: CurveThrough(x, y);	{cubic}
		3: ArcTo(x, y, r);		{radius}
		END;
```
```python
import vs

# Procedure CurveTo creates a bezier vertex point at the specified point.
p = (0, 0)

vs.CurveTo(p)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
