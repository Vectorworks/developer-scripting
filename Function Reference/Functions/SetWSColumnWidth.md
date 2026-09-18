# SetWSColumnWidth

## Description
Sets the width of a column in the referenced worksheet.

SetWSColumnWidth allows width to be set for a range of columns. To set the width of a single worksheet column, specify identical values for the left/right column range boundaries.

```pascal
PROCEDURE SetWSColumnWidth(
				worksheet  : HANDLE;
				fromColumn : INTEGER;
				toColumn   : INTEGER;
				width      : INTEGER);
```

```python
def vs.SetWSColumnWidth(worksheet, fromColumn, toColumn, width):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|fromColumn|INTEGER|Leftmost column of column range.|
|toColumn|INTEGER|Rightmost column of column range.|
|width|INTEGER|New width of columns (in pixels).|

## Examples
```pascal
SetWSPlacement(tempHandle,130,223,698,816);
{SetObjectVariableInt(tempHandle,86,0);} {Don't do this!!!!}
SetObjectVariableInt(tempHandle,87,10);
{Column Widths}
SetWSColumnWidth(tempHandle,1,1,80);
SetWSColumnWidth(tempHandle,2,2,96);
SetWSColumnWidth(tempHandle,3,3,304);
{Cells}
SetWSCellTextFormat(tempHandle,1,1,1,1,DefaultWSFontID,14,1);

IF GetObject(kSeatingCount) = NIL THEN BEGIN
	MyWSHandle := CreateWS(kSeatingCount, 3, 5);
	DefaultWSFontID := GetObjectVariableInt(MyWSHandle,86);
	ShowWS(MyWSHandle, FALSE); {Hide the WS while we create it}
	SetWSColumnWidth   (MyWSHandle, 1, 1, (19 * 12));
	SetWSColumnWidth   (MyWSHandle, 2, 2, (8 * 12));
	SetWSCellTextFormat(MyWSHandle, 1, 1, 1, 5, DefaultWSFontID, 14, 1);

	SetObjectVariableInt    (wsHand, 86, GetFontID('Arial')); {Default Font Index}
	SetObjectVariableInt    (wsHand, 87, 10);     {Default Font Size}
	SetObjectVariableReal   (wsHand, 89, 0.10);   {Left Print Margin}
	SetObjectVariableReal   (wsHand, 91, 0.10);   {Right Print Margin}
	SetWSColumnWidth        (wsHand,  1, kNumCols, 70);
	ShowWS(wsHand, FALSE);
END;
```
```python
import vs

# Sets the width of a column in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
fromColumn = 5
toColumn = 5
width = 1

vs.SetWSColumnWidth(worksheet, fromColumn, toColumn, width)
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [28. Symbol Instance Schedule](ai%20examples/28_WorksheetSymbolSchedule.md), [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
