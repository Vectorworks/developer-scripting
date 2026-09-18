# SetWSCellVertAlignment

## Description
Sets the vertical alignment of cells in the referenced worksheet.

SetWSCellVertAlignment allows a vertical alignment to be set for a range of cells. To set the vertical alignment of a single cell, specify identical values for the top/bottom and left/right range boundaries.

Note:
Vertical alignment constants:
* top = 1
* center  = 3
* bottom = 5

```pascal
PROCEDURE SetWSCellVertAlignment(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				vAlignment  : INTEGER);
```

```python
def vs.SetWSCellVertAlignment(worksheet, topRow, leftColumn, bottomRow, rightColumn, vAlignment):
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
|vAlignment|INTEGER|Vertical alignment index value to be set|

## Examples
```pascal
SetWSCellVertAlignment (wksH, 1, 1, 2, 7, 3);
SetWSCellVertAlignment (wksH, 4, 1, 4, 7, 3);
SetWSCellWrapTextFlag (wksH, 1, 1, 1, 7, FALSE);

SetWSCellAlignment  (wksH, titleRow, 1, titleRow, 3, 2);
SetWSCellAlignment  (wksH, dataBaseRow, 1, dataBaseRow, 1, 2);
SetWSCellAlignment  (wksH, dataBaseRow, 3, dataBaseRow, 3, 2);
SetWSCellVertAlignment (wksH, 1, 1, 2, 3, 3);
SetWSColumnWidth (wksH, 1, 1, otherFieldWidth);
SetWSColumnWidth (wksH, 2, 2, descFieldWidth);
SetWSColumnWidth (wksH, 3, 3, otherFieldWidth);
SetWSCellFormula (wksH, titleRow, 1, titleRow, 1, GetLocStr (16001,  5));	{'Item #'}
```
```python
import vs

# Sets the vertical alignment of cells in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
vAlignment = 1

vs.SetWSCellVertAlignment(worksheet, topRow, leftColumn, bottomRow, rightColumn, vAlignment)
```

## Version
Availability: from VectorWorks 12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
