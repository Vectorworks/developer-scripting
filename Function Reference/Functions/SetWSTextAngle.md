# SetWSTextAngle

## Description
Sets the text angle of a cell the referenced worksheet.

SetWSTextAngle allows text angle to be set for a range of cells. To set the text angle for a single cell, specify identical values for the top/bottom and left/right range boundaries.

Note:
VW12 supports only horizontal text (0 degree) and vertical text (90 degrees).

```pascal
PROCEDURE SetWSTextAngle(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				angle       : INTEGER);
```

```python
def vs.SetWSTextAngle(worksheet, topRow, leftColumn, bottomRow, rightColumn, angle):
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
|angle|INTEGER|New text angle (0 or 90 degrees)|

## Remarks
Note:
VW12 supports only horizontal text (0 degree) and vertical text (90 degrees). So, the input of any angle different from 0 will be handled as 90 degrees in VW12.

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
