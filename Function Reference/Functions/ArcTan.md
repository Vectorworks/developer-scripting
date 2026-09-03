# ArcTan

## Description
Function ArcTan returns the arc tangent (in radians) of the specified value.

```pascal
FUNCTION ArcTan(v : REAL): REAL;
```

```python
def vs.ArcTan(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Numeric value for which to find the tangent.|

## Examples
```pascal
	END;
	objH := LNewObj;
	UpdateTexture(objH, bOpenDoor,  Deg2Rad(45) , Deg2Rad(-45));
EndGroup;
sqrt := Rad2Deg(ArcTan((gLeftLength - gDepth)/(gLength-gDepth))) ;
SET3DRot(LNewObj, 0, 0,sqrt-90, -gDepth,-gLength+gCabThick/2, 0);

IF h = w THEN tanAlpha := 1
ELSE tanAlpha := Tan ( ArcTan ( (-2*Ixy) / (Ixx - Iyy) ) / 2 );

BEGIN
	tmp := rise/theLength;
	tmp := ArcTan(tmp);
	GetGuardRailAngle := Rad2Deg(tmp);
END;
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
