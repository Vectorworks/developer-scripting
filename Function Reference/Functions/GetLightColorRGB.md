# GetLightColorRGB

## Description
Procedure GetLightColorRGB returns the RGB color values for the referenced light object.

```pascal
PROCEDURE GetLightColorRGB(
				light     : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetLightColorRGB(light):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|light|HANDLE|Handle to light.|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Remarks
Color param range is 0..65535 -DLD 8/28/98

## Examples
```pascal
GetBeamAngle(h, R1);
Writeln('Beam Angle:',R1);
GetSpreadAngle(h, R1);
Writeln('Beam Spread:',R1);
GetLightColorRGB(h,R1,R2,R3);
Writeln('Color:',R1,',',R2,',',R3);
GetLightDirection(h,R1,R2);
Writeln('Pan:',R1,' Tilt:',R2);
GetLightFalloff(h,R1,R2);

GetLightColorRGB(LightObjHan,
								gLightRColor[SceneNumber, LightNum],
								gLightGColor[SceneNumber, LightNum],
								gLightBColor[SceneNumber, LightNUm]
							);
```
```python
import vs

# Procedure GetLightColorRGB returns the RGB color values for the referenced
# light object.
light = vs.FSActLayer()  # handle to the first selected object on the active layer

red, green, blue = vs.GetLightColorRGB(light)
vs.Message('GetLightColorRGB returned: ' + str((red, green, blue)))
```

## Version
Availability: from MiniCAD7.0.1

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
