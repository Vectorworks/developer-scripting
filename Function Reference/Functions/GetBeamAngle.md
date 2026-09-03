# GetBeamAngle

## Description
Procedure GetBeamAngle returns the spread angle of the referenced spot light.

```pascal
PROCEDURE GetBeamAngle(
				h              : HANDLE;
				VAR beamAngleR : REAL);
```

```python
def vs.GetBeamAngle(h):
    return beamAngleR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|beamAngleR|REAL|Returns beam spread angle.|

## Examples
```pascal
GetLightLocation(h,R1,R2,R3);
Writeln('Location:',R1,',',R2,',',R3);
GetLightInfo(h,I1,R1,B1,B2);
Writeln('Type:',I1,' Brightness:',I1,' On:',B1,' Shadow:',B2);
GetBeamAngle(h, R1);
Writeln('Beam Angle:',R1);
GetSpreadAngle(h, R1);
Writeln('Beam Spread:',R1);
GetLightColorRGB(h,R1,R2,R3);

GetBeamAngle(LightObjHan, gBeamAngle[SceneNumber, LightNum]);
GetSpreadAngle(LightObjHan, gSpreadAngle[SceneNumber, LightNum]);
```
```python
import vs

# Procedure GetBeamAngle returns the spread angle of the referenced spot light.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetBeamAngle(h)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
