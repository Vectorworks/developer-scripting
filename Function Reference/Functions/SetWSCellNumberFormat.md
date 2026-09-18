# SetWSCellNumberFormat

## Description
Sets the numeric formatting of a cell in the referenced worksheet.

SetWSCellNumberFormat allows numeric formatting to be set for a rectangular range of cells. To set the formatting of a single cell, specify identical values for the top/bottom and left/right range boundaries.

**Table - Worksheet Number Formats**

| Style           | Constant | Meaning of Accuracy                                 |
|-----------------|----------|-----------------------------------------------------|
| General         | 0        |                                                     |
| Fixed Decimal   | 1        | number of decimal places                            |
| DecwCommas      | 2        | number of decimal places                            |
| Scientific      | 3        | number of decimal places                            |
| Fractional      | 4        | largest displayed denominator                       |
| Dimension       | 5        |                                                     |
| Angle           | 6        | corresponds to angular accuracy in units dialog     |
| Date            | 7        | index to a date format, e.g. 3 for 'dmy' or 7 for 'd-mmm-y' |
| Conditional     | 8        |                                                     |
| Dimension Area  | 11       |                                                     |
| Dimension Volume| 12       |                                                     |
| Text            | 13       |                                                     |

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

## Examples
```pascal
SetWSColumnWidth(tempHandle,2,2,96);
SetWSColumnWidth(tempHandle,3,3,304);
{Cells}
SetWSCellTextFormat(tempHandle,1,1,1,1,DefaultWSFontID,14,1);
SetWSCellNumberFormat(tempHandle,1,1,1,1,0,0,'','');
SetWSCellBorder(tempHandle,1,1,1,1,TRUE,TRUE,FALSE,FALSE,FALSE);
SetWSCellFormula(tempHandle,1,1,1,1,kRLwkshtName);

SetWSCellAlignment (wksH2, 1, 2, 1, 2, 1);
SetWSCellAlignment (wksH2, 1, 1, 1, 1, 3);
SetWSCellAlignment (wksH2, r0, 1, r0+1, 5, 2);
SetWSCellNumberFormat (wksH2, r0, 2, r0+1, 5, 2, 4, '', '');

SetWSCellNumberFormat (wksH, 3, 5, 3, 5, 1, 2, '', '');
SetWSCellNumberFormat (wksH, 3, 7, 4, 7, 1, 2, '', '');
```
```python
import vs

# Sets the numeric formatting of a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
style = 0
accuracy = 1
leaderString = 'Example'
trailerString = 'Example'

vs.SetWSCellNumberFormat(worksheet, topRow, leftColumn, bottomRow, rightColumn, style, accuracy, leaderString, trailerString)
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
