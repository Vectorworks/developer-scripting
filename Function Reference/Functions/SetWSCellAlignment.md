# SetWSCellAlignment

## Description
Sets the horizontal alignment of a cell in the referenced worksheet.

SetWSCellAlignment allows a formula to be inserted into a rectangular range of cells. To set the alignment of a single cell, specify identical values for the top/bottom and left/right range boundaries.

Alignment index values for worksheet cells correspond to the horizontal alignment index values for text used by VectorScript.

{| class="wikitable_c"
|+ Table - Worksheet Cell Alignment
! Alignment !! Constant
|- 
| Left
| style="text-align:center"| 1
|- 
| Center
| style="text-align:center"| 2
|- 
| Right
| style="text-align:center"| 3
|- 
| General
| style="text-align:center"| 4
|}

```pascal
PROCEDURE SetWSCellAlignment(
				worksheet     : HANDLE;
				topRow        : INTEGER;
				leftColumn    : INTEGER;
				bottomRow     : INTEGER;
				rightColumn   : INTEGER;
				cellAlignment : INTEGER);
```

```python
def vs.SetWSCellAlignment(worksheet, topRow, leftColumn, bottomRow, rightColumn, cellAlignment):
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
|cellAlignment|INTEGER|The new alignment index value.|

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
