# SetSpreadAngle

## Description
Procedure SetSpreadAngle sets the spread angle of the light object. If the light type is not a spot light, the procedure has no effect on the light.

```pascal
PROCEDURE SetSpreadAngle(
				h            : HANDLE;
				spreadAngleR : REAL);
```

```python
def vs.SetSpreadAngle(h, spreadAngleR):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|spreadAngleR|REAL|Beam spread angle of light.|

## Examples
```pascal
					SetBeamAngle(CurLightHandle, CurLightBeamAngle);
					SetSpreadAngle(CurLightHandle, CurLightSpreadAngle);
IF kNoQTOut THEN Writeln('Light # ',LightNum,' Beam ',CurLightBeamAngle, ',',CurLightSpreadAngle);
					SetLightColorRGB(CurLightHandle,CurLightRCol, CurLightGCol, CurLightBCol);
IF kNoQTOut THEN Writeln('Light # ',LightNum,' Color ',CurLightRCol, ',',CurLightGCol, ',',CurLightBCol);
					IF LightingDeviceHand = NIL THEN

BEGIN
SetBeamAngle(LightObjHandle, gBeamAngle[SceneNumber, LightNumber]);
SetSpreadAngle(LightObjHandle, gSpreadAngle[SceneNumber, LightNumber]);
END;
```
```python
import vs

# Procedure SetSpreadAngle sets the spread angle of the light object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
spreadAngleR = 45.0

vs.SetSpreadAngle(h, spreadAngleR)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
