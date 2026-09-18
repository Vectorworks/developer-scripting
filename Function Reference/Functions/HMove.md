# HMove

## Description
Procedure HMove moves the referenced object a relative offset distance.

```pascal
PROCEDURE HMove(
				h       : HANDLE;
				xOffset : REAL;
				yOffset : REAL);
```

```python
def vs.HMove(h, xOffset, yOffset):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|xOffset|REAL|X offset distance.|
|yOffset|REAL|Y offset distance.|

## Examples
#### VectorScript ####
```pascal
HMove(handleToObject,2,2);
```
#### Python ####
```python
vs.HMove(vs.FSActLayer(),2,2)
```

```pascal
BEGIN
	CreateText(theLabel);
	HCenter(LNewObj, x, y);
	HMove(LNewObj, centerPt[1]-x, centerPt[2]-y);
	SetFPat(LNewObj, 0);
	gNothingDrawn := FALSE;
END;

	ELSE baseH := WholeOval(-gBaseWidth/2, gBaseDepth/2, gBaseWidth/2, -gBaseDepth/2);
END;
Absolute;
IF NOT p__IsPilaster THEN
	HMove (baseH, gOffsetX, gOffsetY);

BEGIN
	Hrotate(ThisHandle, Origin.x, Origin.y, -angle);
	{HMove(ThisHandle, -PX, -PY);} {Don't move to the origin center, object is expected where the user has clicked. [Sasha, 2 July 10]}
	HMove( ThisHandle, mouseX - Origin.x, mouseY );
	SetPref(92, planrotation);
END;
```
```python
import vs

# Procedure HMove moves the referenced object a relative offset distance.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
xOffset = 0.0
yOffset = 0.0

vs.HMove(h, xOffset, yOffset)
```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
