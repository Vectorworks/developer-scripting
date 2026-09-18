# Rad2Deg

## Description
Function Rad2Deg converts the specified value (in radians) to degrees.

```pascal
FUNCTION Rad2Deg(radianValue : REAL): REAL;
```

```python
def vs.Rad2Deg(radianValue):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|radianValue|REAL|Value in radians.|

## Examples
```pascal
	END;
	objH := LNewObj;
	UpdateTexture(objH, bOpenDoor,  Deg2Rad(45) , Deg2Rad(-45));
EndGroup;
sqrt := Rad2Deg(ArcTan((gLeftLength - gDepth)/(gLength-gDepth))) ;
SET3DRot(LNewObj, 0, 0,sqrt-90, -gDepth,-gLength+gCabThick/2, 0);

	IF daylightSavings THEN daylightSavingstmp:=1
	ELSE daylightSavingstmp:=0;
	TrueSolarTime := localTime +
		(Rad2Deg(standardMeridianLongitude - siteLongitude))
		 / 15 +
		equationOfTime - daylightSavingstmp;
END;

Radius := pRadius;
StartingUpright := pStarting_upright;
EndingUpright := pEnding_upright;
FirstAngle := pFirst_Angle;
FirstAngle := 2*Rad2Deg((ArcSin((FirstAngle/2)/Radius)));
UprightAngle := pUpright_Angle;
UprightAngle := 2*Rad2Deg((ArcSin((UprightAngle/2)/Radius)));
UprightWidth := pUpright_width;
UprightDepth := pUpright_depth;
```
```python
if gRFO < gMinFenceOffset:
	gRFO = gMinFenceOffset
	vs.SetRField( gObjHandle, gObjName, 'Right Fence Offset', vs.Num2StrF( gRFO ) )
angDTMMod = 2 * ( vs.Rad2Deg( vs.ArcTan( gMinFenceOffset / ( vs.PRadius ) ) ) )
if vs.PSweep <= 5:
	numSeg = 2
else:
	numSeg = vs.Trunc( vs.PSweep / 5 ) + 1
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
