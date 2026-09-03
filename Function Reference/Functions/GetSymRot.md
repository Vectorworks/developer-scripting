# GetSymRot

## Description
Function GetSymRot returns the rotation angle (in degrees) of the referenced symbol or plug-in object.

```pascal
FUNCTION GetSymRot(symHd : HANDLE): REAL;
```

```python
def vs.GetSymRot(symHd):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symHd|HANDLE|Handle to symbol.|

## Examples
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
if vs.P__Custom_Rot:
	pioRotation = vs.P__Custom_Rot_Value
else:
	pioRotation = vs.GetSymRot( gObjHandle )
```

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
