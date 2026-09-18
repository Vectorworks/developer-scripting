# CreateLight

## Description
CreateLight creates a new light object in the active VectorScript document. 

A new light objects' color is defaulted to white, and brightness is defaulted to 75%. 

**Table - Light Types**

| Light Type   | Constant |
|--------------|----------|
| Directional  | 0        |
| Point        | 1        |
| Spot         | 2        |

```pascal
FUNCTION CreateLight(
				pXR        : REAL;
				pYR        : REAL;
				pZR        : REAL;
				lightType  : INTEGER;
				isOn       : BOOLEAN;
				castShadow : BOOLEAN): HANDLE;
```

```python
def vs.CreateLight(pXR, pYR, pZR, lightType, isOn, castShadow):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pXR|REAL|X coordinate of new light.|
|pYR|REAL|Y coordinate of new light.|
|pZR|REAL|Z coordinate of new light.|
|lightType|INTEGER|Light type.|
|isOn|BOOLEAN|On-off status of light.|
|castShadow|BOOLEAN|Specifies whether light will cast shadow.|

## Examples
#### VectorScript ####
```pascal
CreateLight(2, 3, 8, 1, TRUE, TRUE);
```
#### Python ####
```python
vs.CreateLight(2, 3, 8, 1, True, True)
```

```pascal
BEGIN
	gLightHan := CreateLight(1,1,1,0, TRUE,TRUE);
	IF gShowFrameCounter THEN SetupFrameCounter;
	GetSunrise(gSunriseHour, gSunriseMinute, gDoQTFrames);
	GoTilSunset(gSunriseHour, gSunriseMinute, gSunSetHour, gSunSetMinute, gDoQTFrames);
END;

BEGIN
	z := z + ztmp;
	SetOriginAbsolute(0,0);
	lightHandle := CreateLight(xOrg+x,yOrg+y,z,1,TRUE,TRUE);
	SetOriginAbsolute(xOrg,yOrg);
	DoMenuTextByName( GetLocStr(11050,24), 1 );{'OpenGL Render Chunk'}
	ReDrawAll;
	END;

BEGIN
TmpLightHandle := CreateLight(gLightXLoc[SceneNumber, I], gLightYLoc[SceneNumber, I], gLightZLoc[SceneNumber, I],2,FALSE,TRUE);
IF TmpLightHandle <> NIL THEN
	BEGIN
	SetName(TmpLightHandle,gLightName[SceneNumber, I]);
	TempLightCount := TempLightCount+1;
```
```python
import vs

# CreateLight creates a new light object in the active VectorScript document.
pXR = 1.0
pYR = 2.0
pZR = 0.5
lightType = 0
isOn = True
castShadow = True

objHandle = vs.CreateLight(pXR, pYR, pZR, lightType, isOn, castShadow)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
