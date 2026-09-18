# Stipple

## Description
Greates a group of 'stipple-shapes', objects that fill a 'profile object'

```pascal
FUNCTION Stipple(
				hProfileObject : HANDLE;
				shapeType      : INTEGER;
				density        : INTEGER;
				clipToProfile  : INTEGER;
				minSize        : REAL;
				maxSize        : REAL;
				minAspectRatio : REAL;
				maxAspectRatio : REAL;
				randomRotate   : BOOLEAN): HANDLE;
```

```python
def vs.Stipple(hProfileObject, shapeType, density, clipToProfile, minSize, maxSize, minAspectRatio, maxAspectRatio, randomRotate):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hProfileObject|HANDLE|   |
|shapeType|INTEGER|   |
|density|INTEGER|   |
|clipToProfile|INTEGER|   |
|minSize|REAL|   |
|maxSize|REAL|   |
|minAspectRatio|REAL|   |
|maxAspectRatio|REAL|   |
|randomRotate|BOOLEAN|   |

## Examples
```pascal
	FillBack(Red,Green,Blue);
	ColorIndexToRGB(gStippleColor,Red,Green,Blue);
	PenFore(Red,Green,Blue);
	PenBack(Red,Green,Blue);
	TempH := Stipple(SolidPoly, gStippleShape, gStippleDensity, gStippleClip, gStippleMinSize, gStippleMaxSize, gStippleMinAsp, gStippleMaxAsp, gStippleRand); END;
IF gConfig = 4 THEN
BEGIN
	PenSize(gStippleLW);
	ColorIndexToRGB(gStippleFill,Red,Green,Blue);

BEGIN
IF gShape_1_pct < 100 THEN BEGIN
	BeginGroup;
	temp_h := Stipple(hpoly, gShape_Idx_1, (gShape_1_pct / 100) * density, gClip_Idx, gMin_Size_1*gMult, gMax_Size_1*gMult,1,gMax_Aspect_1,gRandom_Rotate);
	temp_h := Stipple(hpoly, gShape_Idx_2, (1-(gShape_1_pct / 100)) * density, gClip_Idx, gMin_Size_2*gMult, gMax_Size_2*gMult,1,gMax_Aspect_2,gRandom_Rotate);
	EndGroup;
	Stipple_Mix := lNewObj;
	END ELSE Stipple_Mix := Stipple(hpoly, gShape_Idx_1, density, gClip_Idx, gMin_Size_1*gMult, gMax_Size_1*gMult,1,gMax_Aspect_1,gRandom_Rotate);
```
```python
import vs

# Greates a group of 'stipple-shapes', objects that fill a 'profile object'.
hProfileObject = vs.FSActLayer()  # handle to the first selected object on the active layer
shapeType = 0
density = 1
clipToProfile = 2
minSize = 1.0
maxSize = 1.0
minAspectRatio = 1.0
maxAspectRatio = 1.0
randomRotate = True

objHandle = vs.Stipple(hProfileObject, shapeType, density, clipToProfile, minSize, maxSize, minAspectRatio, maxAspectRatio, randomRotate)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
