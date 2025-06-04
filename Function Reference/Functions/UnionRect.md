# UnionRect

## Description
Procedure UnionRect returns a rectangle based on the boundary enclosing the two specified rectangles.

```pascal
PROCEDURE UnionRect(
				p1X,p1Y     : REAL;
				p2X,p2Y     : REAL;
				p3X,p3Y     : REAL;
				p4X,p4Y     : REAL;
				VAR p5X,p5Y : REAL;
				VAR p6X,p6Y : REAL);
```

```python
def vs.UnionRect(p1, p2, p3, p4, p5, p6):
    return (p5, p6)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Top left coordinate of rectangle 1.|
|p2|REAL|Bottom right coordinate of rectangle 1.|
|p3|REAL|Top left coordinate of rectangle 2.|
|p4|REAL|Bottom right coordinate of rectangle 2.|
|p5|REAL|Top left coordinate of boundary rectangle.|
|p6|REAL|Bottom right coordinate of boundary rectangle.|

## Examples
==== VectorScript ====
```pascal
UnionRect(0,0,3,3,3,3,5,5,x1,y1,x2,y2);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
