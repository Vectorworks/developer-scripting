# Sqr

## Description
Function Sqr returns the square of the specified value.

```pascal
FUNCTION Sqr(v : REAL): REAL;
```

```python
def vs.Sqr(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Value to square.|

## Examples
```pascal
BEGIN
	ColorDiff := Sqrt(Sqr(Abs(b2 - b1)) + Sqr(Distance(r1, g1, r2, g2)));
END;

markerPt.x := Str2Num(GetRField(ActiveParmHand,ActiveRecName,kNNA_MarkerLocX));
markerPt.y := Str2Num(GetRField(ActiveParmHand,ActiveRecName,kNNA_MarkerLocY));
textPt.x := Str2Num(GetRField(ActiveParmHand,ActiveRecName,kNNA_TextLocX));
textPt.y := Str2Num(GetRField(ActiveParmHand,ActiveRecName,kNNA_TextLocY));
gShoulderLength := Sqrt( Sqr(shoulderPt.y - markerPt.y) + Sqr(shoulderPt.x - markerPt.x));
END

Draw3DGuard(GuardClass, UprightDepth, sqrt(sqr(theLength) + sqr(Rise)), Overallheight, Rise);
```
```python
import vs

# Function Sqr returns the square of the specified value.
v = 1.0

value = vs.Sqr(v)
vs.Message('Sqr returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
