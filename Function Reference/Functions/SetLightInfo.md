# SetLightInfo

## Description
Sets the attributes of the referenced light object.

```pascal
PROCEDURE SetLightInfo(
				h          : HANDLE;
				lightType  : INTEGER;
				brightness : INTEGER;
				isOn       : BOOLEAN;
				castShadow : BOOLEAN);
```

```python
def vs.SetLightInfo(h, lightType, brightness, isOn, castShadow):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|lightType|INTEGER|Light type.|
|brightness|INTEGER|Brightness of light.|
|isOn|BOOLEAN|On-off status of light.|
|castShadow|BOOLEAN|Shadow casting status of light.|

## Examples
```pascal
						END;
					CurLightIsOn := (CurLightBrightness > 0);
IF kNoQTOut THEN Writeln('Frame #',FrameNumber);
IF kNoQTOut THEN Writeln(Concat('Light # ',LightNum,' On ? ',CurLightIsOn,' Brightness ',CurLightBrightness));
					SetLightInfo(CurLightHandle,
											gLightType[gStartSceneNum, LightNum],
											CurLightBrightness,
											CurLightIsOn,
											gCastShadow[gStartSceneNum, LightNum]
										);

					gLightYLoc[SceneNumber, LightNumber],
					gLightZLoc[SceneNumber, LightNumber]
					);
	END;
SetLightInfo(LightObjHandle,
						gLightType[SceneNumber, LightNumber],
						gBrightNess[SceneNumber, LightNumber],
						gIsOn[SceneNumber, LightNumber],
						gCastShadow[SceneNumber, LightNumber]
					);
IF gLightType[SceneNumber, LightNumber] < 3 THEN
	BEGIN
```
```python
import vs

# Sets the attributes of the referenced light object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
lightType = 0
brightness = 1
isOn = True
castShadow = True

vs.SetLightInfo(h, lightType, brightness, isOn, castShadow)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
