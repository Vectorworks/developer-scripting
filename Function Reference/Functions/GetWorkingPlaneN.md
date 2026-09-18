# GetWorkingPlaneN

## Description
Get the active working plane.

```pascal
PROCEDURE GetWorkingPlaneN(
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
def vs.GetWorkingPlaneN():
    return (outCenterPt, outNormal, outUVec)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outCenterPt|REAL|Output. The working plane center.|
|outNormal|REAL|Output. The working plane normal.|
|outUVec|REAL|Output. The U Vector of the plane.|

## Examples
```pascal
GetWorkingPlaneN(oX,oY,oZ,nX,nY,nZ,uX,uY,uZ);
SetWorkingPlaneN(oX,oY,oZ,nX,nY,nZ,uX,uY,uZ);
{ SetEntitymatrix will be used to set created objects to this plane }

BEGIN
	GetWorkingPlaneN(oX, oY, oZ, nX, nY, nZ, uX, uY, uZ);

BEGIN
	GetWorkingPlaneN( outCenter.x, outCenter.y, outCenter.z, outNormal.x, outNormal.y, outNormal.z, outUVec.x, outUVec.y, outUVec.z );
	theRot:=GetSymRot(gParmH) - Vec2Ang( outUVec );
	if not bRotateText then
	BEGIN
	 	IF (theRot>0) AND (theRot<=90) THEN BEGIN
```
```python
import vs

# Get the active working plane.
outCenterPt, outNormal, outUVec = vs.GetWorkingPlaneN()
vs.Message('GetWorkingPlaneN returned: ' + str((outCenterPt, outNormal, outUVec)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
