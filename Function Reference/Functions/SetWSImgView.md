# SetWSImgView

## Description
Sets specified image view in specified worksheet cells.

```pascal
PROCEDURE SetWSImgView(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				view        : INTEGER);
```

```python
def vs.SetWSImgView(worksheet, topRow, leftColumn, bottomRow, rightColumn, view):
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
|view|INTEGER|The image view.|

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
