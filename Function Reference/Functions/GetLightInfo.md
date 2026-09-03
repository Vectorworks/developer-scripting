# GetLightInfo

## Description
Procedure GetLightInfo returns the attributes of the referenced light object.

**Table - Light Types**

| Light Type   | Constant |
|--------------|----------|
| Directional  | 0        |
| Point        | 1        |
| Spot         | 2        |

```pascal
PROCEDURE GetLightInfo(
				h              : HANDLE;
				VAR lightType  : INTEGER;
				VAR brightness : INTEGER;
				VAR isOn       : BOOLEAN;
				VAR castShadow : BOOLEAN);
```

```python
def vs.GetLightInfo(h):
    return (lightType, brightness, isOn, castShadow)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|lightType|INTEGER|Returns light type.|
|brightness|INTEGER|Returns light brightness.|
|isOn|BOOLEAN|Returns on-off status of light.|
|castShadow|BOOLEAN|Returns whether light casts shadows.|

## Examples
```pascal
	BEGIN
Writeln(Concat('Light Hand:',h));
GetLightLocation(h,R1,R2,R3);
Writeln('Location:',R1,',',R2,',',R3);
GetLightInfo(h,I1,R1,B1,B2);
Writeln('Type:',I1,' Brightness:',I1,' On:',B1,' Shadow:',B2);
GetBeamAngle(h, R1);
Writeln('Beam Angle:',R1);
GetSpreadAngle(h, R1);

		gLightZLoc[SceneNumber, LightNum] := TempLightLocVec.z;
		gIsProjLight[SceneNumber, LightNum] := TRUE;
		END;
	END;
GetLightInfo(LightObjHan,
						gLightType[SceneNumber, LightNum],
						gBrightNess[SceneNumber, LightNum],
						gIsOn[SceneNumber, LightNum],
						gCastShadow[SceneNumber, LightNum]
					);
```
```python
import vs

# Procedure GetLightInfo returns the attributes of the referenced light object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

lightType, brightness, isOn, castShadow = vs.GetLightInfo(h)
vs.Message('GetLightInfo returned: ' + str((lightType, brightness, isOn, castShadow)))
```

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
