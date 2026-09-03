# GetLightFalloff

## Description
Procedure GetLightFalloff returns the fall off attributes for the referenced light object. 

**Table - Light Falloff Types**

| Falloff Type | Constant |
|--------------|----------|
| None         | 0        |
| Normal       | 1        |
| Smooth       | 2        |
| Sharp        | 3        |

```pascal
PROCEDURE GetLightFalloff(
				light           : HANDLE;
				VAR distFalloff : INTEGER;
				VAR angFalloff  : INTEGER);
```

```python
def vs.GetLightFalloff(light):
    return (distFalloff, angFalloff)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|light|HANDLE|Handle to light.|
|distFalloff|INTEGER|Returns distance falloff value.|
|angFalloff|INTEGER|Returns angular falloff value.|

## Remarks
Returns the falloff functions for the light.  0 = None, 1 = Normal, 2 = Smooth, 3 = Sharp (angular falloff only).

## Examples
```pascal
GetLightColorRGB(h,R1,R2,R3);
Writeln('Color:',R1,',',R2,',',R3);
GetLightDirection(h,R1,R2);
Writeln('Pan:',R1,' Tilt:',R2);
GetLightFalloff(h,R1,R2);
Writeln('Fall Dist:',R1,' Fall Ang:',R2);
	END;

GetLightFalloff(LightObjHan,
							gDistFallOff[SceneNumber, LightNum],
							gAngFallOff[SceneNumber, LightNum]
						);
```
```python
import vs

# Procedure GetLightFalloff returns the fall off attributes for the
# referenced light object.
light = vs.FSActLayer()  # handle to the first selected object on the active layer

distFalloff, angFalloff = vs.GetLightFalloff(light)
vs.Message('GetLightFalloff returned: ' + str((distFalloff, angFalloff)))
```

## Version
Availability: from MiniCAD7.0.1

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
