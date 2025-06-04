# GetPrimaryUnitInfo

## Description
Procedure GetPrimaryUnitInfo returns the primary units settings for the active document.

```pascal
PROCEDURE GetPrimaryUnitInfo(
				VAR style    : INTEGER;
				VAR prec     : LONGINT;
				VAR dimPrec  : LONGINT;
				VAR format   : INTEGER;
				VAR angPrec  : INTEGER;
				VAR showMark : BOOLEAN;
				VAR dispFrac : BOOLEAN);
```

```python
def vs.GetPrimaryUnitInfo():
    return (style, prec, dimPrec, format, angPrec, showMark, dispFrac)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|INTEGER|Returns active primary units style.|
|prec|LONGINT|Returns display precision.|
|dimPrec|LONGINT|Returns dimension precision.|
|format|INTEGER|Returns decimal formatting.|
|angPrec|INTEGER|Returns angular precision.|
|showMark|BOOLEAN|Returns unit mark display setting.|
|dispFrac|BOOLEAN|Returns fractional display setting.|

## Remarks
Returns settings information for primary units.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
style              :INTEGER;
prec, dimPrec      :LONGINT;
format, angPrec    :INTEGER;
showMark, dispFrac :BOOLEAN;
major, minor, maintenance, platform :INTEGER;
BEGIN
GetVersion(major, minor, maintenance, platform);
GetPrimaryUnitInfo(style, prec, dimPrec, format, angPrec, showMark, dispFrac);

CASE major of
8: Case style of
    0: AlrtDialog('Custom');
    1: AlrtDialog('Old Style Feet/Inches');
    2: AlrtDialog('Millimeter');
    3: AlrtDialog('Centimeter');
    4: AlrtDialog('Inches');
    5: AlrtDialog('Meters');
    6: AlrtDialog('Feet/Inches');
    7: AlrtDialog('Feet');
    END;

9..11: Case style of
    0: AlrtDialog('Custom');
    1: AlrtDialog('Feet/Inches');
    2: AlrtDialog('Feet');
    3: AlrtDialog('Inches');
    4: AlrtDialog('Millimeters');
    5: AlrtDialog('Centimeters');
    6: AlrtDialog('Meters');
    END;

12: Case style of
    1: AlrtDialog('Feet and Inches');
    2: AlrtDialog('Inches');
    3: AlrtDialog('Feet');
    4: AlrtDialog('Yards');
    5: AlrtDialog('Miles');
    6: AlrtDialog('Microns');
    7: AlrtDialog('Millimeters');
    8: AlrtDialog('Centimeters');
    9: AlrtDialog('Meters');
    10: AlrtDialog('Kilometers');
    11: AlrtDialog('Degrees');
    END;

END;
END; 
RUN(Example);
```
#### Python ####
```python
def Example():
	major, minor, maintenance, platform = vs.GetVersion()
	style, prec, dimPrec, format, angPrec, showMark, dispFrac = vs.GetPrimaryUnitInfo()

	if major == 8:	
		if style == 0: 
			vs.AlrtDialog('Custom')
		elif style == 1: 
			vs.AlrtDialog('Old Style Feet/Inches')
		elif style == 2: 
			vs.AlrtDialog('Millimeter')
		elif style == 3: 
			vs.AlrtDialog('Centimeter')
		elif style == 4: 
			vs.AlrtDialog('Inches')
		elif style == 5: 
			vs.AlrtDialog('Meters')
		elif style == 6: 
			vs.AlrtDialog('Feet/Inches')
		elif style == 7: 
			vs.AlrtDialog('Feet')


	elif major >= 9 and major <= 11:
		if style == 0:  
			vs.AlrtDialog('Custom')
		elif style == 1: 
			vs.AlrtDialog('Feet/Inches')
		elif style == 2: 
			vs.AlrtDialog('Feet')
		elif style == 3: 
			vs.AlrtDialog('Inches')
		elif style == 4: 
			vs.AlrtDialog('Millimeters')
		elif style == 5: 
			vs.AlrtDialog('Centimeters')
		elif style == 6: 
			vs.AlrtDialog('Meters')
	

	elif major == 12: 
		if style == 1:
			vs.AlrtDialog('Feet and Inches')
		elif style == 2: 
			vs.AlrtDialog('Inches')
		elif style == 3: 
			vs.AlrtDialog('Feet')
		elif style == 4: 
			vs.AlrtDialog('Yards')
		elif style == 5: 
			vs.AlrtDialog('Miles')
		elif style == 6: 
			vs.AlrtDialog('Microns')
		elif style == 7: 
			vs.AlrtDialog('Millimeters')
		elif style == 8: 
			vs.AlrtDialog('Centimeters')
		elif style == 9: 
			vs.AlrtDialog('Meters')
		elif style == 10: 
			vs.AlrtDialog('Kilometers')
		elif style == 11: 
			vs.AlrtDialog('Degrees')

Example()
```

## See Also
VS Functions:
[GetRoundingBase](GetRoundingBase.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Units](../Categories/Units.md)
