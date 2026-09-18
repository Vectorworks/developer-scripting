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

## Examples
```pascal
SetWSImgMarginSize(worksheet, 1, 2, 3, 10, 5);
```
```python
import vs

# Sets specified image margin size in specified worksheet cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
marginSize = 1

vs.SetWSImgMarginSize(worksheet, topRow, leftColumn, bottomRow, rightColumn, marginSize)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
