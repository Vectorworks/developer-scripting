# GetArc

## Description
Procedure GetArc returns the start and sweep angle of the referenced arc or round wall.

```pascal
PROCEDURE GetArc(
				h               : HANDLE;
				VAR startAngleR : REAL;
				VAR arcAngleR   : REAL);
```

```python
def vs.GetArc(h):
    return (startAngleR, arcAngleR)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to arc.|
|startAngleR|REAL|Returns start angle of arc.|
|arcAngleR|REAL|Returns sweep angle of arc.|

## Remarks
On round walls, this call won't detect if the wall is reversed or not (should return the inverse of the angle, if the wall is reversed).

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetArcSetArcExample;
VAR
h :HANDLE;
startAng, sweepAng :REAL;
BEGIN
h := FSActLayer;
GetArc(h, startAng, sweepAng);
SetArc(h, startAng, sweepAng + 10);
END;
RUN(GetArcSetArcExample);
```
#### Python ####
```python
def GetArcSetArcExample():
	h = vs.FSActLayer()
	if h != None:
		startAng, sweepAng = vs.GetArc(h)
		vs.SetArc(h, startAng, sweepAng + 10)
GetArcSetArcExample()
```

```pascal
BEGIN
	GetArc(arcHandle, theAngle, theta);
  	HCenter(arcHandle, centerPt[1], centerPt[2]);
	theRadius := HPerim(arcHandle) / Deg2Rad(theta);
	theArcLength := (PI * theRadius * theta) / 180;
	chord := Sin(Deg2Rad(Abs(theta/2))) * theRadius * 2;

BEGIN
	HCenter (objH, x0, y0);
	GetArc (ObjH, theta1, theta2);

{Arc, circle}
6, 7: BEGIN
	GetArc(objH, startAngle, arcAngle);
	IF arcAngle = 360 THEN
		getProperties_Circle (objH, area, perim, xC, yC, Ixx, Iyy, Cxx, Cyy)
	ELSE getProperties_Polyline (objH, area, perim, xC, yC, Ixx, Iyy, Cxx, Cyy);
END;
```
```python
import vs

# Procedure GetArc returns the start and sweep angle of the referenced arc or
# round wall.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

startAngleR, arcAngleR = vs.GetArc(h)
vs.Message('GetArc returned: ' + str((startAngleR, arcAngleR)))
```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
