# SecondaryUnits

## Description
Procedure SecondaryUnits sets the secondary unit parameters for the active document. The secondary units setting is used primarily for display of alternate dimensions when a dual dimension standard is active. 


**Table - Units Formats**

| Units Format         | Constant |
|--------------------- |----------|
| Decimal              | 0        |
| Fractional           | 1        |
| Decimal Ft/Inches    | 2        |
| Fractional Ft/Inches | 3        |

**Table - Standard Unit Settings**

| Units Setting | Constant |
|---------------|----------|
| Custom        | 0        |
| Feet/Inches   | 1        |
| Inches        | 2        |
| Feet          | 3        |
| Yards         | 4        |
| Miles         | 5        |
| Microns       | 6        |
| Millimeters   | 7        |
| Centimeters   | 8        |
| Meters        | 9        |
| Kilometers    | 10       |

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
See [GetPrimaryUnitInfo](GetPrimaryUnitInfo.md) for details on changes in version 9 and again in version 12.

## Examples
#### VectorScript ####
```pascal
SecondaryUnits(1, 6, 2, TRUE, TRUE); 
{ Sets the secondary units to feet/inches with a dimension precision of 1/64, }
{ unit mark displayed, and fractional display of units values enabled.        }
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD 7.0

## Category
* [Units](../Categories/Units.md)
