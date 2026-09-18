# WorksheetMergeCells

## Description
Merges the specified cells into a single cell.

```pascal
FUNCTION WorksheetMergeCells(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER): BOOLEAN;
```

```python
def vs.WorksheetMergeCells(worksheet, topRow, leftColumn, bottomRow, rightColumn):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Worksheet on which function is to operate.|
|topRow|INTEGER|Top row of range to merge.|
|leftColumn|INTEGER|Left column of range to merge.|
|bottomRow|INTEGER|Bottom row of range to merge.|
|rightColumn|INTEGER|Right column of range to merge.|

## Examples
```pascal
{Message(MsgTitle,CR,'Calculating Totals');}
theRow := 5;
ok := WorksheetMergeCells(WSHan,theRow,2,theRow,12);
SetWSCellWrapTextFlag(WSHan,theRow,2,theRow,10,TRUE);
SetWSCellFormula(WSHan,theRow,2,theRow,2,GetPlugInString(4000)); {IMPORTANT!  The table below is created by a vectorscript command.}
SetWSCellFormula(WSHan,theRow+1,2,theRow+1,2,GetPlugInString(4001)); {It will not be recalculated until you issue the "Make Data Cable Count WKS" command again.}
SetWSCellTextFormat(WSHan,theRow,2,theRow+1,2,fontIndex,14,1);

theRow := 5;
SetWSCellFormula(WSHan, theRow, 2, theRow, 2, GetPlugInString(4000)); {The table below is created by a vectorscript command.}
SetWSCellFormula(WSHan, theRow+1, 2, theRow+1, 2, GetPlugInString(4001)); {It will not be recalculated until you issue the "Make Feeder Cable Count WKS" command again.}
SetWSCellTextFormat(WSHan, theRow, 2, theRow+1, 2, fontIndex, 14, 1 );
ok := WorksheetMergeCells(WSHan, theRow, 2, theRow, 11);
ok := WorksheetMergeCells(WSHan, theRow+1, 2, theRow+1, 11);

{	Message(MsgTitle,CR,'Calculating Totals');}
	theRow := 5;
	ok := WorksheetMergeCells(WSHan,theRow,2,theRow,12);
	SetWSCellWrapTextFlag(WSHan,theRow,2,theRow,10,TRUE);
	SetWSCellFormula(WSHan,theRow,2,theRow,2,GetPlugInString(4000)); {IMPORTANT!  The table below is created by a vectorscript command.}
	SetWSCellFormula(WSHan,theRow+1,2,theRow+1,2,GetPlugInString(4001)); {It will not be recalculated until you issue the "Make Jumper Cable Count WKS" command again.}
	SetWSCellTextFormat(WSHan,theRow,2,theRow+1,2,fontIndex,14,1);
```
```python
import vs

# Merges the specified cells into a single cell.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5

ok = vs.WorksheetMergeCells(worksheet, topRow, leftColumn, bottomRow, rightColumn)
if ok:
    vs.Message('WorksheetMergeCells succeeded')
else:
    vs.Message('WorksheetMergeCells failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Worksheets](../Categories/Worksheets.md)
