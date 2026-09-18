# SetWSImgRenderMode

## Description
Sets specified image render mode in specified worksheet cells.

```pascal
PROCEDURE SetWSImgRenderMode(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				renderMode  : INTEGER);
```

```python
def vs.SetWSImgRenderMode(worksheet, topRow, leftColumn, bottomRow, rightColumn, renderMode):
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
|renderMode|INTEGER|The image render mode.|

## Examples
```pascal
SetWSImgRenderMode(worksheet, 1, 2, 3, 10, 5);
```
```python
import vs

# Sets specified image render mode in specified worksheet cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
renderMode = 0

vs.SetWSImgRenderMode(worksheet, topRow, leftColumn, bottomRow, rightColumn, renderMode)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
