# GetSpreadAngle

## Description
Procedure GetSpreadAngle returns the spread angle of the referenced spot light.

```pascal
PROCEDURE GetSpreadAngle(
				h                : HANDLE;
				VAR spreadAngleR : REAL);
```

```python
def vs.GetSpreadAngle(h):
    return spreadAngleR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|spreadAngleR|REAL|Returns spread angle of light.|

## Examples
```pascal
GetLightInfo(h,I1,R1,B1,B2);
Writeln('Type:',I1,' Brightness:',I1,' On:',B1,' Shadow:',B2);
GetBeamAngle(h, R1);
Writeln('Beam Angle:',R1);
GetSpreadAngle(h, R1);
Writeln('Beam Spread:',R1);
GetLightColorRGB(h,R1,R2,R3);
Writeln('Color:',R1,',',R2,',',R3);
GetLightDirection(h,R1,R2);

GetBeamAngle(LightObjHan, gBeamAngle[SceneNumber, LightNum]);
GetSpreadAngle(LightObjHan, gSpreadAngle[SceneNumber, LightNum]);
```
```python
import vs

# Procedure GetSpreadAngle returns the spread angle of the referenced spot light.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetSpreadAngle(h)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
