# SetBeamAngle

## Description
Procedure SetBeamAngle sets the spread angle of the referenced spot light.

```pascal
PROCEDURE SetBeamAngle(
				h          : HANDLE;
				beamAngleR : REAL);
```

```python
def vs.SetBeamAngle(h, beamAngleR):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|beamAngleR|REAL|Beam angle of light.|

## Examples
```pascal
					SetBeamAngle(CurLightHandle, CurLightBeamAngle);
					SetSpreadAngle(CurLightHandle, CurLightSpreadAngle);
IF kNoQTOut THEN Writeln('Light # ',LightNum,' Beam ',CurLightBeamAngle, ',',CurLightSpreadAngle);
					SetLightColorRGB(CurLightHandle,CurLightRCol, CurLightGCol, CurLightBCol);
IF kNoQTOut THEN Writeln('Light # ',LightNum,' Color ',CurLightRCol, ',',CurLightGCol, ',',CurLightBCol);

BEGIN
SetBeamAngle(LightObjHandle, gBeamAngle[SceneNumber, LightNumber]);
SetSpreadAngle(LightObjHandle, gSpreadAngle[SceneNumber, LightNumber]);
END;
```
```python
import vs

# Procedure SetBeamAngle sets the spread angle of the referenced spot light.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
beamAngleR = 45.0

vs.SetBeamAngle(h, beamAngleR)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
