# SprdFormat

## Description
Procedure SprdFormat determines the number format for cells within the active worksheet.

Values for ldr and trailr may not exceed 8 characters.

**Table - Worksheet Cell Formats**

| Cell Format      | Constant |
|------------------|----------|
| General          | 0        |
| Decimal          | 1        |
| Decimal/comma    | 2        |
| Scientific       | 3        |
| Fractional       | 4        |
| Dimension        | 5        |
| Angle            | 6        |

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
#### VectorScript ####
```pascal
SprdFormat(2, 2, '$', '');
LoadCell(1, 1, '=500 * 3.25');
```
#### Python ####
```python

```

## See Also
[SetWSCellNumberFormat](SetWSCellNumberFormat.md)

## Version
SprdFormat is obsolete as of VectorWorks 9.0, see new [SetWSCellNumberFormat](SetWSCellNumberFormat.md).

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
