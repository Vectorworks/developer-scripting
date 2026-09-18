# OLDMassDistStrToReal

## Description
Converts distributed mass string to real number and returns TRUE on success.

```pascal
FUNCTION OLDMassDistStrToReal(
				distrMassString : STRING;
				VAR realValue   : REAL): BOOLEAN;
```

```python
def vs.OLDMassDistStrToReal(distrMassString):
    return (BOOLEAN, realValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|distrMassString|STRING|   |
|realValue|REAL|   |

## Examples
```pascal
BEGIN
	value := GetRField( parmHand, parmName, kStrDistrWeightStr );
	IF OLDMassDistStrToReal( value, valueReal ) THEN
	BEGIN
		SetRField( parmHand, parmName, kStrDistributedWeight, Num2Str( 9, valueReal ) );
	END;

BEGIN
	IF OLDMassDistStrToReal((GetRfield(ghParm, kPIOName,'DistWeight')),NewRealWhole) THEN	{NewRealWhole in GRAMS PER MM}
		BEGIN
			IF NewRealWhole < 0  THEN NewRealWhole := 0;
			SetRField (ghParm, kPIOName, 'DistWeight',Concat(OLDMassDistRealToStr(NewRealWhole)));

HoistWtStr	:= GetRField(HoistHdl,kHoistPIOName,'HoistWt');
isOK	:= OLDMassStrToReal( HoistWtStr, checkVal1 );
ChainWtVal	:= Str2Num(GetRField(HoistHdl,kHoistPIOName,'ChainWtReal'));
ChainWtStr	:= GetRField(HoistHdl,kHoistPIOName,'ChainWt');
isOK	:= OLDMassDistStrToReal( ChainWtStr, checkVal2 );
LoadWtVal	:= Str2Num(GetRField(HoistHdl,kHoistPIOName,'LoadWtReal'));
LoadWtStr	:= GetRField(HoistHdl,kHoistPIOName,'LoadWt');
isOK	:= OLDMassStrToReal( LoadWtStr, checkVal3 );
IF NOT (	Eq( HoistWtVal, checkVal1, 10 )
```
```python
import vs

# Converts distributed mass string to real number and returns TRUE on success.
distrMassString = 'Example'

ok, realValue = vs.OLDMassDistStrToReal(distrMassString)
vs.Message('OLDMassDistStrToReal returned: ' + str((ok, realValue)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
