# GetWSImgSize

## Description
Gets the specified worksheet cell's image size.

```pascal
PROCEDURE GetWSImgSize(
				worksheet  : HANDLE;
				row        : INTEGER;
				column     : INTEGER;
				VAR height : INTEGER;
				VAR width  : INTEGER);
```

```python
def vs.GetWSImgSize(worksheet, row, column):
    return (height, width)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|height|INTEGER|The image height.|
|width|INTEGER|The image width.|

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
