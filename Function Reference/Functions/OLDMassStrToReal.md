# OLDMassStrToReal

## Description
Converts mass string to real number in grams and returns TURE on success. If no unit mark is specified, string is assumed in document units.

```pascal
FUNCTION OLDMassStrToReal(
				massString    : STRING;
				VAR realValue : REAL): BOOLEAN;
```

```python
def vs.OLDMassStrToReal(massString):
    return (BOOLEAN, realValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|massString|STRING|   |
|realValue|REAL|   |

## Examples
```pascal
BEGIN
	IF OLDMassStrToReal(GetRfield(ghParm,kPIOName,'Yoke Weight'),YokeWeightFromOIP) THEN BEGIN END;		{YokeWeightFromOIP in GRAMS}
	IF YokeWeightFromOIP < 0  THEN YokeWeightFromOIP := 0;
	SetRField (ghParm, kPIOName, 'Yoke Weight',Concat(OLDMassRealToStr(YokeWeightFromOIP)));
END

BEGIN
	IF OLDMassStrToReal((GetRfield(ghParm, kPIOName,'BxWeight')),TEMPREAL) THEN BEGIN END;
	IF TEMPREAL < 0  THEN TEMPREAL := 0;
	SetRField (ghParm, kPIOName, 'BxWeight',Concat(OLDMassRealToStr(TEMPREAL)));
	OLDSetLoadDataReal(ghParm,kDLDSelectorWeight,TEMPREAL,0);
	SetRField (ghParm, kPIOName, 'BxWeightKG', Concat(RoundedNumber(TEMPREAL,kWeightMaxDecPoint)));

BEGIN
	OldRealWhole := OldRealWhole*1000;
	IF OLDMassStrToReal((GetRfield(ghParm, kPIOName,'Weight')),NewRealWhole) THEN	{NewRealWhole in GRAMS}
		BEGIN
			IF NewRealWhole < 0  THEN NewRealWhole := 0;
			IF	NOT Eq( NewRealWhole, OldRealWhole, 1 ) THEN
				BEGIN
					OLDSetLoadDataReal(ghParm,kDLDSelPrmTotalDistWght,NewRealWhole,0);
					SetRField (ghParm, kPIOName, 'Weight',Concat(OLDMassRealToStr(NewRealWhole)));
```
```python
import vs

# Converts mass string to real number in grams and returns TURE on success.
massString = 'Example'

ok, realValue = vs.OLDMassStrToReal(massString)
vs.Message('OLDMassStrToReal returned: ' + str((ok, realValue)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
