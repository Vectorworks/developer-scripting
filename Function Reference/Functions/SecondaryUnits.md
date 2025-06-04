# SecondaryUnits

## Description
Procedure SecondaryUnits sets the secondary unit parameters for the active document. The secondary units setting is used primarily for display of alternate dimensions when a dual dimension standard is active. 


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
PROCEDURE SecondaryUnits(
				style    : INTEGER;
				dimPrec  : LONGINT;
				format   : INTEGER;
				showMark : BOOLEAN;
				dispFrac : BOOLEAN);
```

```python
def vs.SecondaryUnits(style, dimPrec, format, showMark, dispFrac):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|INTEGER|Active secondary unit style for document.|
|dimPrec|LONGINT|Dimension precision.|
|format|INTEGER|Decimal formatting.|
|showMark|BOOLEAN|Unit mark display setting.|
|dispFrac|BOOLEAN|Fractional display setting.|

## Remarks
See [[VS:GetPrimaryUnitInfo| GetPrimaryUnitInfo]] for details on changes in version 9 and again in version 12.

## Examples
==== VectorScript ====
```pascal
SecondaryUnits(1, 6, 2, TRUE, TRUE); 
{ Sets the secondary units to feet/inches with a dimension precision of 1/64, }
{ unit mark displayed, and fractional display of units values enabled.        }
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD 7.0

## Category
* [Units](../Categories/Units.md)
