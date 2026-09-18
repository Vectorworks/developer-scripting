# ArcCos

## Description
Function ArcCos returns the arccosine (in radians) of the specified value.

```pascal
FUNCTION ArcCos(v : REAL): REAL;
```

```python
def vs.ArcCos(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Numeric value for which to find the cosine.|

## Examples
```pascal
IF (azimDenom <> 0.0) THEN
	azimuth := arccos(azimNum / azimDenom)
ELSE
	Message(kCalcAzim);
END

slopeAng := ArcCos( dist2DToLast / dist3DToLast );
IF ( dist2DToLast < .1" ) | ( slopeAng > ( maxSlopeAng * 1.5 ) ) THEN BEGIN

BEGIN
	recalculatePhi := TRUE;
	phi := ArcCos ( ( r3^2 + r4^2 - b^2 ) / ( 2 * r3 * r4 ) );
END;
```
```python
import vs

# Function ArcCos returns the arccosine (in radians) of the specified value.
v = 1.0

value = vs.ArcCos(v)
vs.Message('ArcCos returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
