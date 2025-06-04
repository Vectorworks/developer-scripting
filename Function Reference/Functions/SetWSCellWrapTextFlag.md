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

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
