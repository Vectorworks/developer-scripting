# SetWSCellAlignment

## Description
Sets the horizontal alignment of a cell in the referenced worksheet.

SetWSCellAlignment allows a formula to be inserted into a rectangular range of cells. To set the alignment of a single cell, specify identical values for the top/bottom and left/right range boundaries.

Alignment index values for worksheet cells correspond to the horizontal alignment index values for text used by VectorScript.

**Table - Worksheet Cell Alignment**

| Alignment | Constant |
|-----------|----------|
| Left      | 1        |
| Center    | 2        |
| Right     | 3        |
| General   | 4        |

```pascal
PROCEDURE SetWSCellAlignment(
				worksheet     : HANDLE;
				topRow        : INTEGER;
				leftColumn    : INTEGER;
				bottomRow     : INTEGER;
				rightColumn   : INTEGER;
				cellAlignment : INTEGER);
```

```python
def vs.SetWSCellAlignment(worksheet, topRow, leftColumn, bottomRow, rightColumn, cellAlignment):
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
|cellAlignment|INTEGER|The new alignment index value.|

## Examples
```pascal
SetWSCellTextFormat(MyWSHandle, 3, 1, 3, 5, DefaultWSFontID, 12, 1); {Bold 12pt for row 3}
SetWSCellFormula   (MyWSHandle, 3, 1, 3, 1, kTotal);
SetWSCellAlignment (MyWSHandle, 3, 1, 3, 1, 3); {Right Align}

{define the formatting for the main heading}
SetWSColumnWidth(tempHandle, tempA, tempA, Str2Num(gSchFldInfo[tempA, 3])*10); {*10 = characters-to-pixels conversion}
SetWSCellAlignment(tempHandle, 2, tempA, 2, tempA, 1);
SetWSCellTextFormat(tempHandle, 2, tempA, 2, tempA, GetFontID(gSchFontName[1]), gSchTxtSizeInfo[1], 1);

SetWSCellAlignment(gWorkSheetHandle,1,1,1,5,2);
END;
```
```python
import vs

# Sets the horizontal alignment of a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
cellAlignment = 1

vs.SetWSCellAlignment(worksheet, topRow, leftColumn, bottomRow, rightColumn, cellAlignment)
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [28. Symbol Instance Schedule](ai%20examples/28_WorksheetSymbolSchedule.md), [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
