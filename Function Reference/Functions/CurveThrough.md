# CurveThrough

## Description
Procedure CurveThrough fits a cubic spline through the specified point.

```pascal
PROCEDURE CurveThrough(pX,pY : REAL);
```

```python
def vs.CurveThrough(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinates of vertex.|

## Examples
```pascal
AngleVar;
CASE vertexTypeFlag OF
	0 : LineTo (vertexX, #vertexY);
	1 : CurveTo (vertexX, #vertexY);
	2 : CurveThrough (vertexX, #vertexY);
	3 : ArcTo (vertexX, #vertexY, 0);
END;

1: BEGIN
	AddPoint(Offset,0.0);
	CurveThrough(Offset + Scaler*BreakWidth/4,Scaler*BreakHeight/2);
	CurveThrough(Offset + Scaler*3*BreakWidth/4,-1*Scaler*BreakHeight/2);
	AddPoint(Offset + Scaler*BreakWidth,0.0);
	END;

BEGIN
AddPoint(X0-Offset,Y0+ScaleFact*RHeight);
ArcTo(X0+Length/8,Y0+ScaleFact*RHeight,0);
CurveThrough(X0+Length/2,Y0);
ArcTo(X0+7*Length/8,Y0+ScaleFact*RHeight,0);
AddPoint(X0+Length+Offset,Y0+ScaleFact*RHeight);
END
```
```python
import vs

# Procedure CurveThrough fits a cubic spline through the specified point.
p = (0, 0)

vs.CurveThrough(p)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
