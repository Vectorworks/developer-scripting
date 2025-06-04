# SetWSImgUseLayScale

## Description
Sets the worksheet cells' image use layer scale state.

```pascal
PROCEDURE SetWSImgUseLayScale(
				worksheet     : HANDLE;
				topRow        : INTEGER;
				leftColumn    : INTEGER;
				bottomRow     : INTEGER;
				rightColumn   : INTEGER;
				useLayerScale : BOOLEAN);
```

```python
def vs.SetWSImgUseLayScale(worksheet, topRow, leftColumn, bottomRow, rightColumn, useLayerScale):
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
|useLayerScale|BOOLEAN|The user layer scale state.|

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
