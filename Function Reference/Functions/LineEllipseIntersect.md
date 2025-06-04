# LineEllipseIntersect

## Description
Calculates the intersection between the specified line and ellipse.

```pascal
PROCEDURE LineEllipseIntersect(
				a1         : POINT;
				a2         : POINT;
				upperRight : POINT;
				lowerLeft  : POINT;
				VAR int1   : POINT;
				VAR legal1 : BOOLEAN;
				VAR int2   : POINT;
				VAR legal2 : BOOLEAN);
```

```python
def vs.LineEllipseIntersect(a1, a2, upperRight, lowerLeft):
    return (int1, legal1, int2, legal2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|a1|POINT|Start point of the line|
|a2|POINT|End point of the line|
|upperRight|POINT|Upper-right point of the ellipse|
|lowerLeft|POINT|Lower-left point of the ellipse|
|int1|POINT|On return, first point of intersection, if found|
|legal1|BOOLEAN|On return, second point of intersection, if found|
|int2|POINT|On return, indicates that int1 is a valid point of intersection|
|legal2|BOOLEAN|On return, indicates that int2 is a valid point of intersection|

## Remarks
On return, int1 and int2 are the two possible points of intersection.  legal1 and legal2 indicate if the intersections are actually valid.

## Version
Availability: from VectorWorks10.0

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
