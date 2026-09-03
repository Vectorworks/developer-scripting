# GetWSImgScale

## Description
Gets the worksheet cell's image scale.

```pascal
PROCEDURE GetWSImgScale(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER;
				VAR scale : REAL);
```

```python
def vs.GetWSImgScale(worksheet, row, column):
    return scale
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|scale|REAL|The image scale.|

## Examples
```pascal
GetWSImgScale(worksheet, 1, 2, 1.0);
```
```python
import vs

# Gets the worksheet cell's image scale.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSImgScale(worksheet, row, column)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
