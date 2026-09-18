# Round

## Description
Function Round converts the specified REAL value to a LONGINT value. The LONGINT result is the value rounded to the nearest whole number.

```pascal
FUNCTION Round(v : REAL): LONGINT;
```

```python
def vs.Round(v):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Real value to round.|

## Examples
#### VectorScript ####
```pascal
Round(235.24); { returns 235 }
Round(235.73); { returns 236 }
```
#### Python ####
```python

```

```pascal
degrees    := Trunc(inAngle);
tmpDecimal := inAngle - degrees;
minutes    := Trunc(tmpDecimal * 60.0);
tmpDecimal := (tmpDecimal * 60.0) - minutes;
seconds    := Round(tmpDecimal * 60.0);

if ( not btextsPrefEndsAlloc ) then BEGIN
	ALLOCATE textsPrefEnds[1..1,1..2];
	textsPrefEnds[1,1] := GetTextLength( tempH ) - 2;
	textsPrefEnds[1,2] := Round(Str2Num( tmptext[ GetTextLength( tempH ) - 1 ] ));
	btextsPrefEndsAlloc	:= TRUE;
end else BEGIN
	GetArrayDimensions(textsPrefEnds, rowStart, rowEnd, columnStart, columnEnd);
	ALLOCATE textsPrefEnds[1..rowEnd + 1,1..2];

BEGIN
	tempInt := kMinLgthFactor * kFractRound * ( gScrewDia-.001" ) / gUPI;
	minLength := ( tempInt/kFractRound + 1/kFractRound ) * gUPI;
	IF gHeadType < 4 THEN
		minLength := Round( kFractRound*( minLength + gHeadHeight ) ) / kFractRound;
END
```
```python
result = vs.Round(v)
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
