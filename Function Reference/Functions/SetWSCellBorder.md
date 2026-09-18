# SetWSCellBorder

## Description
Sets the borders of a cell in the referenced worksheet.

SetWSCellBorder allows text borders to be set for a rectangular range of cells. To set the border formatting of a single cell, specify identical values for the top/bottom and left/right range boundaries.

```pascal
PROCEDURE SetWSCellBorder(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				top         : BOOLEAN;
				left        : BOOLEAN;
				bottom      : BOOLEAN;
				right       : BOOLEAN;
				outline     : BOOLEAN);
```

```python
def vs.SetWSCellBorder(worksheet, topRow, leftColumn, bottomRow, rightColumn, top, left, bottom, right, outline):
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
|top|BOOLEAN|Top border ON-OFF status.|
|left|BOOLEAN|Left border ON-OFF status.|
|bottom|BOOLEAN|Bottom border ON-OFF status.|
|right|BOOLEAN|Right border ON-OFF status.|
|outline|BOOLEAN|All borders ON-OFF status.|

## Examples
```pascal
SetWSColumnWidth(tempHandle,3,3,304);
{Cells}
SetWSCellTextFormat(tempHandle,1,1,1,1,DefaultWSFontID,14,1);
SetWSCellNumberFormat(tempHandle,1,1,1,1,0,0,'','');
SetWSCellBorder(tempHandle,1,1,1,1,TRUE,TRUE,FALSE,FALSE,FALSE);
SetWSCellFormula(tempHandle,1,1,1,1,kRLwkshtName);

{schedule title}
SetWSCellBorder    (tempHandle, 1, 1, 1, 1, FALSE, FALSE, FALSE, FALSE, FALSE);
SetWSCellTextFormat(tempHandle, 1, 1, 1, 1, GetFontID(gSchFontName[1]), gSchTxtSizeInfo[1], 1);
SetWSCellFormula   (tempHandle, 1, 1, 1, 1, Concat(' ', wsName));

	END
ELSE{It's probably the same worksheer with new data.  Preserve user col widths}
	IsNewWS := FALSE;
ClearWSCell(WSHand,1, 1,nRows, nCols);
SetWSCellBorder(WSHand,1,1,nRows, nCols,FALSE,False,False,False,False);
SetWSCellNumberFormat(WSHand, 1, 1,nRows, nCols, 13, 0,'','');
END
```
```python
import vs

# Sets the borders of a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
top = True
left = True
bottom = True
right = True
outline = True

vs.SetWSCellBorder(worksheet, topRow, leftColumn, bottomRow, rightColumn, top, left, bottom, right, outline)
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## See Also
[SetWSCellBorders](SetWSCellBorders.md)

## Version
SetWSCellBorder is obsolete as of VectorWorks 12.0, see new [ SetWSCellBorders](SetWSCellBorders.md)

Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
