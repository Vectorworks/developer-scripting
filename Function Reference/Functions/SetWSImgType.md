# SetWSImgType

## Description
Sets the worksheet cells' image type.

```pascal
PROCEDURE SetWSImgType(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				type        : INTEGER);
```

```python
def vs.SetWSImgType(worksheet, topRow, leftColumn, bottomRow, rightColumn, type):
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
|type|INTEGER|The image type.|

## Examples
```pascal
SetWSImgType(worksheet, 1, 2, 3, 10, 5);
```
```python
import vs

# Sets the worksheet cells' image type.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
type = 0

vs.SetWSImgType(worksheet, topRow, leftColumn, bottomRow, rightColumn, type)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
