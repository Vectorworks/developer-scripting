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

## Examples
```pascal
GetWorkingPlaneN(oX,oY,oZ,nX,nY,nZ,uX,uY,uZ);
SetWorkingPlaneN(oX,oY,oZ,nX,nY,nZ,uX,uY,uZ);
{ SetEntitymatrix will be used to set created objects to this plane }

BEGIN
	SetWorkingPlaneN(oX, oY, oZ, nX, nY, nZ, uX, uY, uZ);
	GetLayerElevation(ActLayer, layerElevation, layerThickness);
	layerElevation := layerElevation/(25.4 / GetPrefReal( 152 ));
	SetObjectVariableInt(gRedlinePathObjHan,803,0);	{ 0 for 2D }
	SetPlanarRef(gRedlinePathObjHan, GetCurrentPlanarRefID);

BEGIN
	SetWorkingPlaneN(oX, oY, oZ, nX, nY, nZ, uX, uY, uZ);
	GetLayerElevation(ActLayer, layerElevation, layerThickness);
	layerElevation := layerElevation/(25.4 / GetPrefReal( 152 ));
	{ We need to specify pluginObjH as 2D so it will work with Planar APIs SetPlanarRef  }
	SetObjectVariableInt(pluginObjH,803,0);	{ 0 for 2D }
```
```python
import vs

# Set the active working plane.
centerPt = (0, 0)
normal = 'Example'
uVec = 'Example'

vs.SetWorkingPlaneN(centerPt, normal, uVec)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
