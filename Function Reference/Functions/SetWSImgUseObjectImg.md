# SetWSImgUseObjectImg

## Description
Set state of worksheet cell's use object image..

```pascal
PROCEDURE SetWSImgUseObjectImg(
				worksheet      : HANDLE;
				topRow         : INTEGER;
				leftColumn     : INTEGER;
				bottomRow      : INTEGER;
				rightColumn    : INTEGER;
				useObjectImage : BOOLEAN);
```

```python
def vs.SetWSImgUseObjectImg(worksheet, topRow, leftColumn, bottomRow, rightColumn, useObjectImage):
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
|useObjectImage|BOOLEAN|The use object image state.|

## Examples
```pascal
SetWSImgUseObjectImg(worksheet, 1, 2, 3, 10, TRUE);
```
```python
import vs

# Set state of worksheet cell's use object image.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
useObjectImage = True

vs.SetWSImgUseObjectImg(worksheet, topRow, leftColumn, bottomRow, rightColumn, useObjectImage)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
