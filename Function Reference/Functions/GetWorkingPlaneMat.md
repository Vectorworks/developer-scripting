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

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
