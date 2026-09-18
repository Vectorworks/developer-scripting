# ScreenPlanePtToPlanarPt

## Description
Projects a 2D point from the screen plane onto the specified plane.

```pascal
PROCEDURE ScreenPlanePtToPlanarPt(
				refID     : LONGINT;
				pt2D      : REAL;
				VAR outPt : REAL);
```

```python
def vs.ScreenPlanePtToPlanarPt(refID, pt2D):
    return outPt
```

## Parameters
|Name|Type|Description|
|---|---|---|
|refID|LONGINT|Reference ID of the plane.|
|pt2D|REAL|Input the 2D point on the screen.|
|outPt|REAL|Output the 2D point on the plane.|

## Examples
```pascal
ScreenPlanePtToPlanarPt(1, 1.0, 2.0);
```
```python
import vs

# Projects a 2D point from the screen plane onto the specified plane.
refID = 1
pt2D = 1.0

result = vs.ScreenPlanePtToPlanarPt(refID, pt2D)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
