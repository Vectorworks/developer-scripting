# EllipseEllipseIntersect

## Description
Calculates the intersections between the two specified ellipses.

```pascal
FUNCTION EllipseEllipseIntersect(
				upperLeft1  : POINT;
				lowerRight1 : POINT;
				upperLeft2  : POINT;
				lowerRight2 : POINT;
				VAR int1    : POINT;
				VAR int2    : POINT;
				VAR int3    : POINT;
				VAR int4    : POINT): INTEGER;
```

```python
def vs.EllipseEllipseIntersect(upperLeft1, lowerRight1, upperLeft2, lowerRight2):
    return (INTEGER, int1, int2, int3, int4)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|upperLeft1|POINT|Upper-left point of the first ellipse|
|lowerRight1|POINT|Lower-right point of the first ellipse|
|upperLeft2|POINT|Upper-left point of the second ellipse|
|lowerRight2|POINT|Lower-right point of the second ellipse|
|int1|POINT|On return, first point of intersection, if found|
|int2|POINT|On return, second point of intersection, if found|
|int3|POINT|On return, third point of intersection, if found|
|int4|POINT|On return, fourth point of intersection, if found|

## Remarks
On return, int1, int2, int3, and int4 contain the points of intersection.  Return value indicates which intersections are legal.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h1, h2 :HANDLE;
upperLeft1, lowerRight1 :POINT;
upperLeft2, lowerRight2 :POINT;
int1, int2, int3, int4 :POINT;
num :INTEGER;
BEGIN
CallTool(-205); h1 := FSActLayer;
CallTool(-205); h2 := FSActLayer;
GetBBox(h1, upperLeft1.x, upperLeft1.y, lowerRight1.x, lowerRight1.y);
GetBBox(h2, upperLeft2.x, upperLeft2.y, lowerRight2.x, lowerRight2.y);
num := EllipseEllipseIntersect(upperLeft1, lowerRight1, upperLeft2, lowerRight2, int1, int2, int3, int4);
Message(num);
Locus(int1.x, int1.y);
Locus(int2.x, int2.y);
Locus(int3.x, int3.y);
Locus(int4.x, int4.y);
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	vs.OvalN(0, 0, 1, 0, 1, 1);
	h1 = vs.LActLayer()
	vs.OvalN(0, 0.5, 1, 0, 1, 1);
	h2 = vs.LActLayer()
	upperLeft1, lowerRight1 = vs.GetBBox(h1)
	upperLeft2, lowerRight2 = vs.GetBBox(h2)
	num,  int1, int2, int3, int4 = vs.EllipseEllipseIntersect(upperLeft1, lowerRight1, upperLeft2, lowerRight2)
	vs.Message(num)
	vs.Locus(int1[0], int1[1])
	vs.Locus(int2[0], int2[1])
	vs.Locus(int3[0], int3[1])
	vs.Locus(int4[0], int4[1])

Example()
```

## Version
Availability: from VectorWorks10.0

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
