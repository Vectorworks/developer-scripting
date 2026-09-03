# SetViewVector

## Description
Sets the view direction of the active document.

```pascal
PROCEDURE SetViewVector(
				locationX,locationY,locationZ : REAL;
				targetX,targetY,targetZ       : REAL;
				upX,upY,upZ                   : REAL);
```

```python
def vs.SetViewVector(location, target, up):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|location|REAL|3D coordinate of view origin.|
|target|REAL|3D coordinate of view target.|
|up|REAL|3D coordinate indicating camera up direction.|

## Examples
```pascal
BEGIN
{GetView(rotx,roty,rotz,temp_r,temp_r,temp_r);}
{let's assume the next line rotates the object back to a top view by default...}
IF NOT(viewindex = 0) THEN SetViewVector(0,0,0,0,0,-1,0,1,0);
CASE viewIndex OF
	1:	BEGIN {top}
		{should have to do nothing here}
		END;

SetViewVector	(
				CameraPt3D.x,
				CameraPt3D.y,
				CameraPt3D.z,
				TargetPt3D.x,
				TargetPt3D.y,
				TargetPt3D.z,
				CameraUpPt3D.x - CameraPt3D.x,
				CameraUpPt3D.y - CameraPt3D.y,
				CameraUpPt3D.z - CameraPt3D.z
				);
```
```python
import vs

# Sets the view direction of the active document.
location = (0, 0)
target = 'Example'
up = 'Example'

vs.SetViewVector(location, target, up)
```

## Version
Availability: from VectorWorks9.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
