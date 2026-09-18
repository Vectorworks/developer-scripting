# GetLightDirection

## Description
Procedure GetLightDirection returns the direction angles of the referenced light object.

```pascal
PROCEDURE GetLightDirection(
				h              : HANDLE;
				VAR panAngleR  : REAL;
				VAR tiltAngleR : REAL);
```

```python
def vs.GetLightDirection(h):
    return (panAngleR, tiltAngleR)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|panAngleR|REAL|Returns light pan angle.|
|tiltAngleR|REAL|Returns light tilt angle.|

## Examples
```pascal
GetSpreadAngle(h, R1);
Writeln('Beam Spread:',R1);
GetLightColorRGB(h,R1,R2,R3);
Writeln('Color:',R1,',',R2,',',R3);
GetLightDirection(h,R1,R2);
Writeln('Pan:',R1,' Tilt:',R2);
GetLightFalloff(h,R1,R2);
Writeln('Fall Dist:',R1,' Fall Ang:',R2);
	END;

GetLightDirection(LightObjHan,
								gPanDeg[SceneNumber, LightNum],
								gTiltDeg[SceneNumber, LightNum]
							);
```
```python
import vs

# Procedure GetLightDirection returns the direction angles of the referenced
# light object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

panAngleR, tiltAngleR = vs.GetLightDirection(h)
vs.Message('GetLightDirection returned: ' + str((panAngleR, tiltAngleR)))
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
