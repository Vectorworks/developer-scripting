# GetWorkingPlaneMat

## Description
Get the specified working plane matrix.

```pascal
PROCEDURE GetWorkingPlaneMat(
				refID             : LONGINT;
				VAR outCenterPt_x : REAL;
				VAR outCenterPt_y : REAL;
				VAR outCenterPt_z : REAL;
				VAR outNormal_x   : REAL;
				VAR outNormal_y   : REAL;
				VAR outNormal_z   : REAL;
				VAR outUVec_x     : REAL;
				VAR outUVec_y     : REAL;
				VAR outUVec_z     : REAL);
```

```python
def vs.GetWorkingPlaneMat(refID):
    return (outCenterPt, outNormal, outUVec)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|refID|LONGINT|Reference ID of the working plane.|
|outCenterPt|REAL|Output. The working plane center.|
|outNormal|REAL|Output. The working plane normal.|
|outUVec|REAL|Output. The U Vector of the plane.|

## Examples
```pascal
GetWorkingPlaneMat(1, 1.0, 2.0, 0.5, 1.5, 3.0, 1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Get the specified working plane matrix.
refID = 1

outCenterPt, outNormal, outUVec = vs.GetWorkingPlaneMat(refID)
vs.Message('GetWorkingPlaneMat returned: ' + str((outCenterPt, outNormal, outUVec)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
