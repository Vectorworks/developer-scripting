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

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
