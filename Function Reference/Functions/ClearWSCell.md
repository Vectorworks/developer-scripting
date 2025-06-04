# ClearWSCell

## Description
Clears content and resets attributes of a cell in the referenced worksheet.

ClearWSCell allows a rectangular range of cells to be reset. To reset a single cell, specify identical values for the top/bottom and left/right range boundaries.

```pascal
PROCEDURE ClearWSCell(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER);
```

```python
def vs.ClearWSCell(worksheet, topRow, leftColumn, bottomRow, rightColumn):
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

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
