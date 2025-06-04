# SetWSCellNumberFormat

## Description
Sets the numeric formatting of a cell in the referenced worksheet.

SetWSCellNumberFormat allows numeric formatting to be set for a rectangular range of cells. To set the formatting of a single cell, specify identical values for the top/bottom and left/right range boundaries.

{| class="wikitable_c"
|+ Table - Worksheet Number Formats
! Style !! Constant !! Meaning of Accuracy
|- 
| General
| style="text-align:center"| 0
| 
|- 
| Fixed Decimal
| style="text-align:center"| 1
| number of decimal places
|- 
| DecwCommas
| style="text-align:center"| 2
| number of decimal places
|- 
| Scientific
| style="text-align:center"| 3
| number of decimal places
|- 
| Fractional
| style="text-align:center"| 4
| largest displayed denominator
|-  
| Dimension
| style="text-align:center"| 5
| 
|- 
| Angle
| style="text-align:center"| 6
| corresponds to angular accuracy in units dialog
|- 
| Date
| style="text-align:center"| 7
| index to a date format, e.g. 3 for 'dmy' or 7 for 'd-mmm-y' 
|-  
| Conditional
| style="text-align:center"| 8
| 
|- 
| Dimension Area
| style="text-align:center"| 11
| 
|- 
| Dimension Volume
| style="text-align:center"| 12
| 
|- 
| Text
| style="text-align:center"| 13
| 
|}

```pascal
PROCEDURE SetWSCellNumberFormat(
				worksheet     : HANDLE;
				topRow        : INTEGER;
				leftColumn    : INTEGER;
				bottomRow     : INTEGER;
				rightColumn   : INTEGER;
				style         : INTEGER;
				accuracy      : INTEGER;
				leaderString  : STRING;
				trailerString : STRING);
```

```python
def vs.SetWSCellNumberFormat(worksheet, topRow, leftColumn, bottomRow, rightColumn, style, accuracy, leaderString, trailerString):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|topRow|INTEGER|Top row of cell range.|
|leftColumn|INTEGER|Leftmost column of cell range.|
|bottomRow|INTEGER|Bottom row of cell range.|
|rightColumn|INTEGER|Rightmost column of cell range.|
|style|INTEGER|Numeric format style index.|
|accuracy|INTEGER|Numeric accuracy / secondary format index.|
|leaderString|STRING|Leader string (where applicable).|
|trailerString|STRING|Trailer string (where applicable).|

## Remarks
FYI:  DO NOT USE 9 and 10!!!
* General Frac = 9 is used for fraction with unreduced denominator. 
* Dimension With Divider  = 10  is the same as Dimension but for use in output-only situations where the current units format is feet and inches and you want a feet and inch divider.

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
