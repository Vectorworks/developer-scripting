# SetLightDirection

## Description
Procedure SetLightDirection sets the direction angles of the referenced light object.

```pascal
PROCEDURE SetLightDirection(
				h          : HANDLE;
				panAngleR  : REAL;
				tiltAngleR : REAL);
```

```python
def vs.SetLightDirection(h, panAngleR, tiltAngleR):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|panAngleR|REAL|Pan angle of light.|
|tiltAngleR|REAL|Tilt angle of light.|

## Examples
```pascal
BEGIN
	IF gLightHan <> NIL Then SetLightDirection(gLightHan, fAzim, fElev);
	IF gShowFrameCounter THEN
	BEGIN
		If gDaylightSavingsOn then fDisplayStr := Concat(Num2Str(0, fHour-1), ' : ') ELSE fDisplayStr := Concat(Num2Str(0, fHour), ' : ');
		IF fMinute < 10 THEN fDisplayStr := Concat(fDisplayStr, '0');

IF kNoQTOut THEN Writeln('Light # ',LightNum,' Beam ',CurLightBeamAngle, ',',CurLightSpreadAngle);
					SetLightColorRGB(CurLightHandle,CurLightRCol, CurLightGCol, CurLightBCol);
IF kNoQTOut THEN Writeln('Light # ',LightNum,' Color ',CurLightRCol, ',',CurLightGCol, ',',CurLightBCol);
					IF LightingDeviceHand = NIL THEN
						SetLightDirection(CurLightHandle, CurLightPanDeg, CurLightTiltDeg )
					ELSE
						BEGIN
						IF DataExchangeSuspend THEN SetRField(LightingDeviceHand,kInstObjName,kNoExport,'True');
						LDevice_ResetVisual(LightingDeviceHand);
						END;

	IF DataExchangeSuspend THEN SetRField(LightingDeviceHand,kInstObjName,kNoExport,'True');
	ResetObject(LightingDeviceHand);
	END
ELSE
	SetLightDirection(LightObjHandle,
								gPanDeg[SceneNumber, LightNumber],
								gTiltDeg[SceneNumber, LightNumber]
							);
SetLightFalloff(LightObjHandle,
							gDistFallOff[SceneNumber, LightNumber],
							gAngFallOff[SceneNumber, LightNumber]
						);
```
```python
import vs

# Procedure SetLightDirection sets the direction angles of the referenced
# light object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
panAngleR = 45.0
tiltAngleR = 90.0

vs.SetLightDirection(h, panAngleR, tiltAngleR)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
