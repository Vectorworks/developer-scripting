# SetWSCellWrapTextFlag

## Description
Sets the wrap text state of cells in the referenced worksheet.

SetWSCellWrapTextFlag allows wrap text to be set for a range of cells. To set wrap text in a single cell, specify identical values for the top/bottom and left/right range boundaries.
If the wrap text flag is &quot;TRUE&quot; in a cell, text will wrap at the cell border

```pascal
PROCEDURE SetWSCellWrapTextFlag(
				worksheet    : HANDLE;
				topRow       : INTEGER;
				leftColumn   : INTEGER;
				bottomRow    : INTEGER;
				rightColumn  : INTEGER;
				wrapTextFlag : BOOLEAN);
```

```python
def vs.SetWSCellWrapTextFlag(worksheet, topRow, leftColumn, bottomRow, rightColumn, wrapTextFlag):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|topRow|INTEGER|Top row of cell range|
|leftColumn|INTEGER|Left column of cell range|
|bottomRow|INTEGER|Bottom row of cell range|
|rightColumn|INTEGER|Right column of cell range|
|wrapTextFlag|BOOLEAN|Wrap text flag to be set|

## Examples
```pascal
SetWSCellVertAlignment (wksH, 1, 1, 2, 7, 3);
SetWSCellVertAlignment (wksH, 4, 1, 4, 7, 3);
SetWSCellWrapTextFlag (wksH, 1, 1, 1, 7, FALSE);

{Message(MsgTitle,CR,'Calculating Totals');}
theRow := 5;
ok := WorksheetMergeCells(WSHan,theRow,2,theRow,12);
SetWSCellWrapTextFlag(WSHan,theRow,2,theRow,10,TRUE);
SetWSCellFormula(WSHan,theRow,2,theRow,2,GetPlugInString(4000)); {IMPORTANT!  The table below is created by a vectorscript command.}
SetWSCellFormula(WSHan,theRow+1,2,theRow+1,2,GetPlugInString(4001)); {It will not be recalculated until you issue the "Make Data Cable Count WKS" command again.}
SetWSCellTextFormat(WSHan,theRow,2,theRow+1,2,fontIndex,14,1);
ok := WorksheetMergeCells(WSHan,theRow,2,theRow,10);

{	Message(MsgTitle,CR,'Calculating Totals');}
	theRow := 5;
	ok := WorksheetMergeCells(WSHan,theRow,2,theRow,12);
	SetWSCellWrapTextFlag(WSHan,theRow,2,theRow,10,TRUE);
	SetWSCellFormula(WSHan,theRow,2,theRow,2,GetPlugInString(4000)); {IMPORTANT!  The table below is created by a vectorscript command.}
	SetWSCellFormula(WSHan,theRow+1,2,theRow+1,2,GetPlugInString(4001)); {It will not be recalculated until you issue the "Make Jumper Cable Count WKS" command again.}
	SetWSCellTextFormat(WSHan,theRow,2,theRow+1,2,fontIndex,14,1);
	ok := WorksheetMergeCells(WSHan,theRow,2,theRow,10);
```
```python
import vs

# Sets the wrap text state of cells in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
wrapTextFlag = True

vs.SetWSCellWrapTextFlag(worksheet, topRow, leftColumn, bottomRow, rightColumn, wrapTextFlag)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
