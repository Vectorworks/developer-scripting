# SetWSImgMarginSize

## Description
Sets specified image margin size in specified worksheet cells.

```pascal
PROCEDURE SetWSImgMarginSize(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				marginSize  : INTEGER);
```

```python
def vs.SetWSImgMarginSize(worksheet, topRow, leftColumn, bottomRow, rightColumn, marginSize):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|topRow|INTEGER|Top row of cell range.|
|leftColumn|INTEGER|Left column of cell range.|
|bottomRow|INTEGER|Bottom row of cell range.|
|rightColumn|INTEGER|Right column of cell range.|
|marginSize|INTEGER|The image margin size.|

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
