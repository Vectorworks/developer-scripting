# SetWSCellOutlineBN

## Description
Outlines the specified worksheet cells with the specified border.<BR>
<BR>
SetWSCellOutlineBN allows borders to be set for a rectangular range of cells. To set the border formatting of a single cell, specify identical values for the top/bottom and left/right range boundaries.<BR>
<BR>
Note:<BR>
A rectangular range of cells is formatted as a single block of cells. If you apply a top border to the range of cells, the border is displayed only on the right edge of the cells.

```pascal
PROCEDURE SetWSCellOutlineBN(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				style       : LONGINT;
				weight      : INTEGER;
				color       : LONGINT);
```

```python
def vs.SetWSCellOutlineBN(worksheet, topRow, leftColumn, bottomRow, rightColumn, style, weight, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Worksheet on which function is to operate.|
|topRow|INTEGER|Top row of range to set.|
|leftColumn|INTEGER|Left column of range to set.|
|bottomRow|INTEGER|Bottom row of range to set.|
|rightColumn|INTEGER|Right column of range to set.|
|style|LONGINT|Border line style to be set.(0 = None; 2 = Solid; for dashed, use negative value of Internal Index of dash line type|
|weight|INTEGER|Border line weight to be set.(in Mils)|
|color|LONGINT|Border line color to be set. (color index: 0..255)|

## Version
Availability: from Vectorworks 2019

## Category
* [Worksheets](../Categories/Worksheets.md)
