# PrimaryUnits

## Description
Procedure PrimaryUnits specifies the primary units settings for the active document. The primary units setting is used by the document for all measurement entry and display values in the document. 


{| class="wikitable" style="float: right;"
|+ Table - Units Formats
! Units Format
! Constant
|-
| Decimal
| style="text-align:center"| 0
|-
| Fractional
| style="text-align:center"| 1
|-
| Decimal Ft/Inches
| style="text-align:center"| 2
|-
| Fractional Ft/Inches
| style="text-align:center"| 3
|}
{| class="wikitable_c"
|+ Table - Standard Unit Settings
! Units Setting !! Constant
|-
| Custom
| style="text-align:center"| 0
|-
| Feet/Inches
| style="text-align:center"| 1
|-
| Inches
| style="text-align:center"| 2
|-
| Feet
| style="text-align:center"| 3
|-
| Yards
| style="text-align:center"| 4
|-
| Miles
| style="text-align:center"| 5
|-
| Microns
| style="text-align:center"| 6
|-
| Millimeters
| style="text-align:center"| 7
|-
| Centimeters
| style="text-align:center"| 8
|-
| Meters
| style="text-align:center"| 9
|-
| Kilometers
| style="text-align:center"| 10
|}

```pascal
PROCEDURE PrimaryUnits(
				style    : INTEGER;
				prec     : LONGINT;
				dimPrec  : LONGINT;
				format   : INTEGER;
				angPrec  : INTEGER;
				showMark : BOOLEAN;
				dispFrac : BOOLEAN);
```

```python
def vs.PrimaryUnits(style, prec, dimPrec, format, angPrec, showMark, dispFrac):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|INTEGER|Active primary unit style for document.|
|prec|LONGINT|Display precision.|
|dimPrec|LONGINT|Dimension precision.|
|format|INTEGER|Decimal formatting.|
|angPrec|INTEGER|Angular precision.|
|showMark|BOOLEAN|Unit mark display setting.|
|dispFrac|BOOLEAN|Fractional display setting.|

## Remarks
[sd 8/18/98]
See [[VS:GetPrimaryUnitInfo| GetPrimaryUnitInfo]] for details on changes in VW9 and again in VW12.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
style :INTEGER;
prec, dimPrec :LONGINT;
format, angPrec :INTEGER;
showMark, dispFrac :BOOLEAN;
outStr :STRING;
BEGIN
outStr := '';
GetPrimaryUnitInfo(style, prec, dimPrec, format, angPrec, showMark, dispFrac);
FOR style := 0 to 16 DO BEGIN
PrimaryUnits(style, prec, dimPrec, format, angPrec, showMark, dispFrac);
outStr := Concat(outStr, Chr(13), style, ': ', GetPrefReal(152));
END;
AlrtDialog(outStr);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD 7.0

## Category
* [Units](../Categories/Units.md)
