# SetWSImgScale

## Description
Sets specified image scale in specified worksheet cells.

```pascal
PROCEDURE SetWSImgScale(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				scale       : REAL);
```

```python
def vs.SetWSImgScale(worksheet, topRow, leftColumn, bottomRow, rightColumn, scale):
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
|scale|REAL|The image scale.|

## Examples
```pascal
SetWSImgScale(worksheet, 1, 2, 3, 10, 1.0);
```
```python
import vs

# Sets specified image scale in specified worksheet cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
scale = 1.0

vs.SetWSImgScale(worksheet, topRow, leftColumn, bottomRow, rightColumn, scale)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
