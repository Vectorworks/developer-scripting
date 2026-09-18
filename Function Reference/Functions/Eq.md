# Eq

## Description
Returns TRUE if the two real numbers are equal within the tolerance.

```pascal
FUNCTION Eq(
				value1    : REAL;
				value2    : REAL;
				tolerance : REAL): BOOLEAN;
```

```python
def vs.Eq(value1, value2, tolerance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|value1|REAL|   |
|value2|REAL|   |
|tolerance|REAL|   |

## Examples
```pascal
BEGIN
	IF ( NOT Eq( gNewColumnHeight, pOA_Height, Fuzzer ) ) THEN
	BEGIN
		SetRField( formatHand, gPluginName, 'NewHeight', Num2StrF( pOA_Height ) );
		SetRField( formatHand, gPluginName, 'OldHeight', Num2StrF( pOA_Height ) );
		gNewColumnHeight := pOA_Height;
		gOldColumnHeight := pOA_Height;
	END;

BEGIN
GetPolyPt(hPathObj, i, vert.X, vert.Y);
IF NOT (EQ(AngCheck,Vec2Ang(vert),AngFuzz)) THEN
BEGIN
	LinePath := FALSE;
	I := NumVerts+1;
	END;

BEGIN
Found := FALSE;
ForEachObjectInList(FindLoci,0,2,FInSymDef( SymDefHand ));
IF ( (Found) AND ( NOT ( EQ ( Distance(0,0,PitchPt.x,PitchPt.y), 0 , 0.0000001)))) THEN {VB-104891}
	BEGIN
	GetPitchFromSymbol := Distance(0,0,PitchPt.x,PitchPt.y);
	END
```
```python
import vs

# Returns TRUE if the two real numbers are equal within the tolerance.
value1 = 1.0
value2 = 2.0
tolerance = 0.5

ok = vs.Eq(value1, value2, tolerance)
if ok:
    vs.Message('Eq succeeded')
else:
    vs.Message('Eq failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
