# SetWSImgSize

## Description
Sets specified image size in specified worksheet cells.

```pascal
PROCEDURE SetWSImgSize(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				height      : INTEGER;
				width       : INTEGER);
```

```python
def vs.SetWSImgSize(worksheet, topRow, leftColumn, bottomRow, rightColumn, height, width):
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
|height|INTEGER|The image height.|
|width|INTEGER|The image width.|

## Examples
```pascal
SetWSImgSize(worksheet, 1, 2, 3, 10, 5, 1);
```
```python
import vs

# Sets specified image size in specified worksheet cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
height = 1
width = 2

vs.SetWSImgSize(worksheet, topRow, leftColumn, bottomRow, rightColumn, height, width)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
