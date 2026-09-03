# OLDMassRealToStr

## Description
Converts mass real value to string and returns the result.

```pascal
FUNCTION OLDMassRealToStr(massValue : REAL): STRING;
```

```python
def vs.OLDMassRealToStr(massValue):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|massValue|REAL|   |

## Examples
```pascal
BEGIN
	IF OLDMassStrToReal(GetRfield(ghParm,kPIOName,'Yoke Weight'),YokeWeightFromOIP) THEN BEGIN END;		{YokeWeightFromOIP in GRAMS}
	IF YokeWeightFromOIP < 0  THEN YokeWeightFromOIP := 0;
	SetRField (ghParm, kPIOName, 'Yoke Weight',Concat(OLDMassRealToStr(YokeWeightFromOIP)));
END

&	NOT Eq( realVal, oldVal, 1 )		{"&" <> "|"}
THEN BEGIN
	realVal	:= oldVal * 1000;
	OLDSetLoadDataReal( ghParm, kDLDSelectorWeight, realVal, 0 );
	SetRField (ghParm, kPIOName, 'BumpWeight',Concat(OLDMassRealToStr(realVal)));
END;

&	NOT Eq( realVal, oldVal, 1 )		{"&" <> "|"}
THEN BEGIN
	realVal	:= oldVal * 1000;
	OLDSetLoadDataReal( ghParm, kDLDSelectorWeight, realVal, 0 );
	SetRField (ghParm, kPIOName, 'BxWeight',Concat(OLDMassRealToStr(realVal)));
END;
```
```python
import vs

# Converts mass real value to string and returns the result.
massValue = 1.0

text = vs.OLDMassRealToStr(massValue)
vs.Message('OLDMassRealToStr returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
