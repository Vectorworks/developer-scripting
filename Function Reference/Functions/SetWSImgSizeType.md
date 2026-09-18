# SetWSImgSizeType

## Description
Sets specified image size type in specified worksheet cells.

```pascal
PROCEDURE SetWSImgSizeType(
				worksheet     : HANDLE;
				topRow        : INTEGER;
				leftColumn    : INTEGER;
				bottomRow     : INTEGER;
				rightColumn   : INTEGER;
				imageSizeType : INTEGER);
```

```python
def vs.SetWSImgSizeType(worksheet, topRow, leftColumn, bottomRow, rightColumn, imageSizeType):
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
|imageSizeType|INTEGER|The image size type. (0 = automatic, 1 = fixed, 2 = custom scale)|

## Examples
```pascal
SetWSImgSizeType(worksheet, 1, 2, 3, 10, 5);
```
```python
import vs

# Sets specified image size type in specified worksheet cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
imageSizeType = 0

vs.SetWSImgSizeType(worksheet, topRow, leftColumn, bottomRow, rightColumn, imageSizeType)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
