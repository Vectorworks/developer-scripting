# HCenter

## Description
Procedure HCenter returns the logical center point of the object specified in h. For most objects, this is the center of the bounding box. For circles, arcs, and round walls HCenter returns the arc center of the object.

```pascal
PROCEDURE HCenter(
				h         : HANDLE;
				VAR pX,pY : REAL);
```

```python
def vs.HCenter(h):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|p|REAL|X-Y location of object center.|

## Examples
```pascal
BEGIN
	GetArc(arcHandle, theAngle, theta);
  	HCenter(arcHandle, centerPt[1], centerPt[2]);
	theRadius := HPerim(arcHandle) / Deg2Rad(theta);
	theArcLength := (PI * theRadius * theta) / 180;
	chord := Sin(Deg2Rad(Abs(theta/2))) * theRadius * 2;
	T := theRadius * Tan(Deg2Rad(theta/2));

BEGIN
	HCenter (objH, x0, y0);
	GetArc (ObjH, theta1, theta2);

		END;
END;
EndGroup;
ThisHandle := LNewObj;
HCenter(ThisHandle, Origin.x, Origin.y);
PopAttrs;
IF (ThisHandle <> NIL) THEN
BEGIN
	Hrotate(ThisHandle, Origin.x, Origin.y, -angle);
```
```python
import vs

# Procedure HCenter returns the logical center point of the object specified
# in h.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.HCenter(h)
```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
