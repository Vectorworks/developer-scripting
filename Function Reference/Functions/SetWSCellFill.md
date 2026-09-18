# SetWSCellFill

## Description
Sets the fill style and color of a cell in the referenced worksheet

SetWSCellFill allows cell fill style and color text to be set for a range of cells. To set fill style and color for a single cell, specify identical values for the top/bottom and left/right range boundaries.

```pascal
PROCEDURE SetWSCellFill(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				style       : INTEGER;
				bgcolor     : LONGINT;
				fgcolor     : LONGINT;
				fillpattern : INTEGER);
```

```python
def vs.SetWSCellFill(worksheet, topRow, leftColumn, bottomRow, rightColumn, style, bgcolor, fgcolor, fillpattern):
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
|style|INTEGER|Cell fill style to be set|
|bgcolor|LONGINT|Cell background color index value to be set|
|fgcolor|LONGINT|Cell foreground color index value to be set|
|fillpattern|INTEGER|Cell pattern index value to be set|

## Remarks
bgcolor - cell background color  (0 if none)
fgcolor	- cell foreground color   (0 if none)
fillpattern - cell fill pattern index  (-1 if none)

Fill style constants:
no fill = 0
solid fill= 1
pattern fill= 2

## Examples
```pascal
theRow := TheRow +  3;
SetWSCellFormula(WSHan, TheRow, 2, TheRow, 2, GetPlugInString(4019)); {Cable Type, Connectors}
ok := WorksheetMergeCells(WSHan, TheRow, 2, TheRow, 5);
SetWSCellFill(WSHan, TheRow, 2, TheRow, 5, 1,  64, 0, 1) ;
```
```python
import vs

# Sets the fill style and color of a cell in the referenced worksheet
# SetWSCellFill allows cell fill style and color text to be set for a range
# of cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
style = 0
bgcolor = 5
fgcolor = 5
fillpattern = 1

vs.SetWSCellFill(worksheet, topRow, leftColumn, bottomRow, rightColumn, style, bgcolor, fgcolor, fillpattern)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
