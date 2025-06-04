# ArcByCenter

## Description
Creates an arc using a center point, the radius, a start angle, and a sweep.

```pascal
PROCEDURE ArcByCenter(
				x          : REAL;
				y          : REAL;
				radius     : REAL;
				startAngl  : REAL;
				sweepAngle : REAL);
```

```python
def vs.ArcByCenter(x, y, radius, startAngl, sweepAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x|REAL|X-coordinate of the center point|
|y|REAL|Y-coordinate of the center point|
|radius|REAL|Radius of the arc|
|startAngl|REAL|Starting angle of the arc|
|sweepAngle|REAL|Sweep angle of the arc|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
x, y, radius, startAngle, sweepAngle :REAL;
BEGIN
GetPt(x, y);
radius := 3;
startAngle := 0;
sweepAngle := 90;
ArcByCenter(x, y, radius, startAngle, sweepAngle);
AlrtDialog(Concat(GetType(LNewObj)));
END;
RUN(Example);
```
#### Python ####
```python
def PickPointCallback(pt):
	radius = 3
	startAngle = 0
	sweepAngle = 90
	vs.ArcByCenter(pt[0], pt[1], radius, startAngle, sweepAngle)
	vs.AlrtDialog(vs.Concat(vs.GetType(vs.LNewObj())));
vs.GetPt( PickPointCallback )
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
