# PlanarPtToScreenPlanePt

## Description
Projects a 2D point from the specified plane onto the screen plane.

```pascal
FUNCTION PlanarPtToScreenPlanePt(
				refID     : LONGINT;
				pt2D      : REAL;
				VAR outPt : REAL): BOOLEAN;
```

```python
def vs.PlanarPtToScreenPlanePt(refID, pt2D):
    return (BOOLEAN, outPt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|refID|LONGINT|Reference ID of the plane.|
|pt2D|REAL|Input the 2D point on the plane.|
|outPt|REAL|Output the 2D point on the screen.|

## Examples
```pascal
resultOK := PlanarPtToScreenPlanePt(1, 1.0, 2.0);
```
```python
import vs

# Projects a 2D point from the specified plane onto the screen plane.
refID = 1
pt2D = 1.0

ok, outPt = vs.PlanarPtToScreenPlanePt(refID, pt2D)
vs.Message('PlanarPtToScreenPlanePt returned: ' + str((ok, outPt)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
