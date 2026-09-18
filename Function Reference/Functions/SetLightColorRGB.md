# SetLightColorRGB

## Description
Procedure SetLightColorRGB sets the RGB color values for the referenced light object.

```pascal
PROCEDURE SetLightColorRGB(
				light : HANDLE;
				red   : LONGINT;
				green : LONGINT;
				blue  : LONGINT);
```

```python
def vs.SetLightColorRGB(light, red, green, blue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|light|HANDLE|Handle to light.|
|red|LONGINT|RGB color component value.|
|green|LONGINT|RGB color component value.|
|blue|LONGINT|RGB color component value.|

## Remarks
Color param range is 0..65535 -DLD 8/28/98

## Examples
```pascal
					SetBeamAngle(CurLightHandle, CurLightBeamAngle);
					SetSpreadAngle(CurLightHandle, CurLightSpreadAngle);
IF kNoQTOut THEN Writeln('Light # ',LightNum,' Beam ',CurLightBeamAngle, ',',CurLightSpreadAngle);
					SetLightColorRGB(CurLightHandle,CurLightRCol, CurLightGCol, CurLightBCol);
IF kNoQTOut THEN Writeln('Light # ',LightNum,' Color ',CurLightRCol, ',',CurLightGCol, ',',CurLightBCol);
					IF LightingDeviceHand = NIL THEN
						SetLightDirection(CurLightHandle, CurLightPanDeg, CurLightTiltDeg )
					ELSE

	BEGIN
	SetBeamAngle(LightObjHandle, gBeamAngle[SceneNumber, LightNumber]);
	SetSpreadAngle(LightObjHandle, gSpreadAngle[SceneNumber, LightNumber]);
	END;
SetLightColorRGB(LightObjHandle,
								gLightRColor[SceneNumber, LightNumber],
								gLightGColor[SceneNumber, LightNumber],
								gLightBColor[SceneNumber, LightNumber]
							);
IF LightingDeviceHand <> NIL THEN
BEGIN
	IF DataExchangeSuspend THEN SetRField(LightingDeviceHand,kInstObjName,kNoExport,'True');
```
```python
import vs

# Procedure SetLightColorRGB sets the RGB color values for the referenced
# light object.
light = vs.FSActLayer()  # handle to the first selected object on the active layer
red = 65535
green = 0
blue = 0

vs.SetLightColorRGB(light, red, green, blue)
```

## Version
Availability: from MiniCAD7.0.1

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
