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

## Version
Availability: from VectorWorks 12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
