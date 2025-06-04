# SprdFormat

## Description
Procedure SprdFormat determines the number format for cells within the active worksheet.

Values for ldr and trailr may not exceed 8 characters.

{| class="wikitable_c"
|+ Table - Worksheet Cell Formats
! Cell Format !! Constant
|- 
| General
| style="text-align:center"| 0
|- 
| Decimal
| style="text-align:center"| 1
|- 
| Decimal/comma
| style="text-align:center"| 2
|- 
| Scientific
| style="text-align:center"| 3
|- 
| Fractional
| style="text-align:center"| 4
|- 
| Dimension
| style="text-align:center"| 5
|- 
| Angle
| style="text-align:center"| 6
|}

```pascal
PROCEDURE SprdFormat(
				numForm : INTEGER;
				acc     : INTEGER;
				ldr     : STRING;
				trailr  : STRING);
```

```python
def vs.SprdFormat(numForm, acc, ldr, trailr):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|numForm|INTEGER|Numeric format of cell.|
|acc|INTEGER|Numeric accuracy setting.|
|ldr|STRING|String prefix for cell.|
|trailr|STRING|String suffix for cell.|

## Examples
==== VectorScript ====
```pascal
SprdFormat(2, 2, '$', '');
LoadCell(1, 1, '=500 * 3.25');
```
==== Python ====
```python

```

## See Also
[SetWSCellNumberFormat| SetWSCellNumberFormat](SetWSCellNumberFormat|%20SetWSCellNumberFormat.md)

## Version
SprdFormat is obsolete as of VectorWorks 9.0, see new [[VS:SetWSCellNumberFormat| SetWSCellNumberFormat]].

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
