# GetView

## Description
Returns information about the current 3D view.

```pascal
PROCEDURE GetView(
				VAR xAngleR                 : REAL;
				VAR yAngleR                 : REAL;
				VAR zAngleR                 : REAL;
				VAR offsetX,offsetY,offsetZ : REAL);
```

```python
def vs.GetView():
    return (xAngleR, yAngelR, zAngleR, offset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xAngleR|REAL|Returns X rotation angle of view.|
|yAngleR|REAL|Returns Y rotation angle of view.|
|zAngleR|REAL|Returns Z rotation angle of view.|
|offset|REAL|Center of view rotation.|

## Remarks
Returns information about the current 3D view.<br />
All parameters are for output:
:xAngleR, the angle the view is rotated away from the x-axis
:yAngleR, the angle the view is rotated away from the y-axis
:zAngleR, the angle the view is rotated away from the z-axis
:offsetX, Y, and Z, the center of the view

(MaKro, 2016.10.18):<br />
Use [[VS:GetProjection|GetProjection]](ActLayer) == 6 and xyzAngleR == 0 to check if the view is Top/Plan

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
xAngleR, yAngleR, zAngleR, offsetX, offsetY, offsetZ :REAL;
BEGIN
GetView(xAngleR, yAngleR, zAngleR, offsetX, offsetY, offsetZ);
Message(xAngleR, ' ', yAngleR, ' ', zAngleR, ' ', offsetX, ' ', offsetY, ' ', offsetZ);
END;
RUN(Example);
```
Another example:
```pascal
PROCEDURE Example;
VAR
xAngleR, yAngleR, zAngleR, offsetX, offsetY, offsetZ :REAL;
viewNameStr :STRING;
BEGIN
GetView(xAngleR, yAngleR, zAngleR, offsetX, offsetY, offsetZ);
IF (xAngleR =    0) & (yAngleR =    0)    & (zAngleR =    0) THEN viewNameStr := 'Top or Top/Plan'            ELSE
IF (xAngleR =  -90) & (yAngleR =    0)    & (zAngleR =    0) THEN viewNameStr := 'Front'                      ELSE
IF (xAngleR =  -90) & (yAngleR =  -90)    & (zAngleR =    0) THEN viewNameStr := 'Right'                      ELSE
IF (xAngleR =  180) & (yAngleR =    0)    & (zAngleR =    0) THEN viewNameStr := 'Bottom'                     ELSE
IF (xAngleR =   90) & (yAngleR =    0)    & (zAngleR =  180) THEN viewNameStr := 'Back'                       ELSE
IF (xAngleR =  -90) & (yAngleR =   90)    & (zAngleR =    0) THEN viewNameStr := 'Left'                       ELSE
IF (xAngleR =  -45) & Eq(yAngleR, -35, 1) & (zAngleR =  -30) THEN viewNameStr := 'Right Isometric'            ELSE
IF (xAngleR =  -45) & Eq(yAngleR,  35, 1) & (zAngleR =   30) THEN viewNameStr := 'Left Isometric'             ELSE
IF (xAngleR =   45) & Eq(yAngleR, -35, 1) & (zAngleR = -150) THEN viewNameStr := 'Right Rear Isometric'       ELSE
IF (xAngleR =   45) & Eq(yAngleR,  35, 1) & (zAngleR =  150) THEN viewNameStr := 'Left Rear Isometric'        ELSE
IF (xAngleR = -135) & Eq(yAngleR, -35, 1) & (zAngleR =   30) THEN viewNameStr := 'Lower Right Isometric'      ELSE
IF (xAngleR = -135) & Eq(yAngleR,  35, 1) & (zAngleR =  -30) THEN viewNameStr := 'Lower Left Isometric'       ELSE
IF (xAngleR =  135) & Eq(yAngleR, -35, 1) & (zAngleR =  150) THEN viewNameStr := 'Lower Right Rear Isometric' ELSE
IF (xAngleR =  135) & Eq(yAngleR,  35, 1) & (zAngleR = -150) THEN viewNameStr := 'Lower Left Rear Isometric';
Message(
xAngleR, ' ', 
yAngleR, ' ', 
zAngleR, '    ',
offsetX, ' ', 
offsetY, ' ', 
offsetZ, '  view name: ', 
viewNameStr);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	xAngleR, yAngleR, zAngleR, offsetPt = vs.GetView()
	vs.Message(xAngleR, ' ', yAngleR, ' ', zAngleR, ' ', offsetPt[0], ' ', offsetPt[1], ' ', offsetPt[2])

Example()
```

## Version
Availability: from VectorWorks8.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
