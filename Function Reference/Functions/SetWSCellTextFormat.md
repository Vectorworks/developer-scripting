# SetWSCellTextFormat

## Description
Sets text format settings for a cell in the referenced worksheet.

SetWSCellTextFormat allows text formatting to be set for a rectangular range of cells. To set the formatting of a single cell, specify identical values for the top/bottom and left/right range boundaries.

**Table - Text Style**

| Style     | Constant |
|-----------|----------|
| Plain     | 0        |
| Bold      | 1        |
| Italic    | 2        |
| Underline | 4        |
| Outline   | 8        |
| Shadowed  | 16       |

```pascal
PROCEDURE SetWSCellTextFormat(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				fontIndex   : INTEGER;
				size        : INTEGER;
				style       : INTEGER);
```

```python
def vs.SetWSCellTextFormat(worksheet, topRow, leftColumn, bottomRow, rightColumn, fontIndex, size, style):
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
|fontIndex|INTEGER|Font index for cell text.|
|size|INTEGER|Font size for cell text.|
|style|INTEGER|Font style for cell text.|

## Examples
```pascal
SetWSColumnWidth(tempHandle,1,1,80);
SetWSColumnWidth(tempHandle,2,2,96);
SetWSColumnWidth(tempHandle,3,3,304);
{Cells}
SetWSCellTextFormat(tempHandle,1,1,1,1,DefaultWSFontID,14,1);
SetWSCellNumberFormat(tempHandle,1,1,1,1,0,0,'','');
SetWSCellBorder(tempHandle,1,1,1,1,TRUE,TRUE,FALSE,FALSE,FALSE);
SetWSCellFormula(tempHandle,1,1,1,1,kRLwkshtName);

DefaultWSFontID := GetObjectVariableInt(MyWSHandle,86);
ShowWS(MyWSHandle, FALSE); {Hide the WS while we create it}
SetWSColumnWidth   (MyWSHandle, 1, 1, (19 * 12));
SetWSColumnWidth   (MyWSHandle, 2, 2, (8 * 12));
SetWSCellTextFormat(MyWSHandle, 1, 1, 1, 5, DefaultWSFontID, 14, 1);

	{SelectSS(hWS);{activate and Open to Show single change}
	GetWSCellTextFormat( WSh, row, col, fontIdx, fontSize, fontStyle );
	ReplaceStr(str,gFindString,gReplString,gCase);
	SetWSCellFormula( WSh, row, col, row, col, gResultText );
	SetWSCellTextFormat(WSh,row,col,row,col,fontIdx,fontSize,fontStyle);
	ProcessFoundCell := TRUE;
END;
```
```python
import vs

# Sets text format settings for a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
fontIndex = 1
size = 1
style = 0

vs.SetWSCellTextFormat(worksheet, topRow, leftColumn, bottomRow, rightColumn, fontIndex, size, style)
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [28. Symbol Instance Schedule](ai%20examples/28_WorksheetSymbolSchedule.md), [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
