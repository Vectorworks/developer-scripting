# HRotate

## Description
Procedure HRotate rotates the referenced object about a coordinate point location. rotationAngle is in degrees.

```pascal
PROCEDURE HRotate(
				h               : HANDLE;
				centerX,centerY : REAL;
				rotationAngle   : REAL);
```

```python
def vs.HRotate(h, center, rotationAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|center|REAL|X-Y coordinates of center point of rotation.|
|rotationAngle|REAL|Angle of rotation.|

## Examples
#### VectorScript ####
```pascal
HRotate(objHd,3,5,60d);
```
#### Python ####
```python
def Example():
	vs.HRotate(vs.FSActLayer(),3,5,60)

Example()
```

```pascal
BEGIN
	SysBeep;
	createErrorMessage2 (errorText, x0, y0);
	HRotate (LNewObj, x0, y0, -GetSymRot (pluginH));
	getData := FALSE;
END	{of NOT validPathAndFile}

BEGIN
	getData := FALSE;
	createErrorMessage2( errorText, kErrMsgTextSize, GetFontID( kErrMsgTextFont ), kErrMsgWidth, gX0, gY0, kBeep );
	HRotate( LNewObj, gX0, gY0, -GetSymRot( gPluginH ) );
END

BEGIN
	SysBeep;
	createErrorMessage2 (errorText, x0, y0);
	HRotate (LNewObj, x0, y0, -GetSymRot (pluginH));
	getData := FALSE;
END
```
```python
import vs

# Procedure HRotate rotates the referenced object about a coordinate point
# location.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
center = (0, 0)
rotationAngle = 45.0

vs.HRotate(h, center, rotationAngle)
```

## Version
Availability: from MiniCAD6.0

## Category
* [Object Editing](../Categories/Object%20Editing.md)
