# LineLineIntersection

## Description
Returns intersection point of the two specified lines.  parallel is true if the lines are parallel. intOnLines is true if the intersection is on both lines.

```pascal
PROCEDURE LineLineIntersection(
				l1start        : POINT;
				l1end          : POINT;
				l2start        : POINT;
				l2end          : POINT;
				VAR parallel   : BOOLEAN;
				VAR intOnLines : BOOLEAN;
				VAR sectpt     : POINT);
```

```python
def vs.LineLineIntersection(l1start, l1end, l2start, l2end):
    return (parallel, intOnLines, sectpt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|l1start|POINT|Start point of the first line|
|l1end|POINT|End point of the first line|
|l2start|POINT|Start point of the second line|
|l2end|POINT|End point of the second line|
|parallel|BOOLEAN|On return, true if the lines are parallel, false otherwise|
|intOnLines|BOOLEAN|On return, true if the intersection point (if it exists) lies on both of the lines|
|sectpt|POINT|On return, point of intersection of the lines, if the lines intersect|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
pt1, pt2, pt3, pt4, pt5 :POINT;
parallel, intOnLines :BOOLEAN; 

BEGIN
CallTool(-201); 
GetSegPt1(FSActLayer, pt1.x, pt1.y); 
GetSegPt2(FSActLayer, pt2.x, pt2.y); 
CallTool(-201); 
GetSegPt1(FSActLayer, pt3.x, pt3.y); 
GetSegPt2(FSActLayer, pt4.x, pt4.y); 
LineLineIntersection(pt1, pt2, pt3, pt4, parallel, intOnLines, pt5); 
Locus(pt5.x, pt5.y);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
