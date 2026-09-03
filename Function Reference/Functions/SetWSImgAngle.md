# SetWSImgAngle

## Description
Sets specified image angle in specified worksheet cells.

```pascal
PROCEDURE SetWSImgAngle(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				angle       : REAL);
```

```python
def vs.SetWSImgAngle(worksheet, topRow, leftColumn, bottomRow, rightColumn, angle):
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
|angle|REAL|The image angle.|

## Examples
```pascal
SetWSImgAngle(worksheet, 1, 2, 3, 10, 1.0);
```
```python
import vs

# Sets specified image angle in specified worksheet cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
angle = 45.0

vs.SetWSImgAngle(worksheet, topRow, leftColumn, bottomRow, rightColumn, angle)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
