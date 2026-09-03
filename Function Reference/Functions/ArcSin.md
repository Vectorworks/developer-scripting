# ArcSin

## Description
Function ArcSin returns the arc sine (in radians) of the specified value.

```pascal
FUNCTION ArcSin(v : REAL): REAL;
```

```python
def vs.ArcSin(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Numeric value for which to find the sine.|

## Examples
```pascal
BEGIN
	p := Sqrt (t * (2 * rtA - t));
	alpha := ArcSin ((rtA - t) / rtA);
	beta := (PI/2 - alpha) / 2;
	p1 := p - rtA * Tan (beta);
END ELSE
	p1 := 0;

BEGIN
	alpha := 2 * ArcSin (segLength / (2 * r));
	nSegs := Deg2Rad (theta2) / alpha;
END

elevation := arcsin(sin(latitude) * sin(declination) -
					cos(latitude) * cos(declination) * cos(hourAngle));
if ((hourAngle > 0) AND (hourAngle <= PI)) THEN
	BEGIN
	azimNum := -sin(latitude) * sin(elevation) + sin(declination);
	azimDenom := cos(latitude) * cos(elevation);
```
```python
import vs

# Function ArcSin returns the arc sine (in radians) of the specified value.
v = 1.0

value = vs.ArcSin(v)
vs.Message('ArcSin returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
