# SetWSCellTextColor

## Description
Sets the text color of a cell in the referenced worksheet

SetWSCellTextColor allows text color to be set for a range of cells. To set the text color for a single cell, specify identical values for the top/bottom and left/right range boundaries.

```pascal
PROCEDURE SetWSCellTextColor(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				color       : LONGINT);
```

```python
def vs.SetWSCellTextColor(worksheet, topRow, leftColumn, bottomRow, rightColumn, color):
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
|color|LONGINT|Text color index value to be set|

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
