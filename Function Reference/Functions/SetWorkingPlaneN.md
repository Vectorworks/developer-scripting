# SetWorkingPlaneN

## Description
Set the active working plane.

```pascal
PROCEDURE SetWorkingPlaneN(
				VAR CenterPt_x : REAL;
				VAR CenterPt_y : REAL;
				VAR CenterPt_z : REAL;
				VAR Normal_x   : REAL;
				VAR Normal_y   : REAL;
				VAR Normal_z   : REAL;
				VAR UVec_x     : REAL;
				VAR UVec_y     : REAL;
				VAR UVec_z     : REAL);
```

```python
def vs.SetWorkingPlaneN(centerPt, normal, uVec):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|centerPt|REAL|Location of the working plane.|
|normal|REAL|Normal vector of the working plane.|
|uVec|REAL|The U Vector of the plane.|

## Remarks
(\_c\_ 2022.05.12): From Raymond Mullin: as of VW 2022 any working plane set with this routine doesn't persist after script's end. This routine works in this fashion since VW 2011.

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
