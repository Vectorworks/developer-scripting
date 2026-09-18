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

## Examples
```pascal
GetWSImgSize(worksheet, 1, 2, 3, 10);
```
```python
import vs

# Gets the specified worksheet cell's image size.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

height, width = vs.GetWSImgSize(worksheet, row, column)
vs.Message('GetWSImgSize returned: ' + str((height, width)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
