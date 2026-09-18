# GetWSImgMarginSize

## Description
Gets the worksheet cell's image margin size.

```pascal
PROCEDURE GetWSImgMarginSize(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				VAR marginSize : INTEGER);
```

```python
def vs.GetWSImgMarginSize(worksheet, row, column):
    return marginSize
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|marginSize|INTEGER|The image margin size.|

## Examples
```pascal
GetWSImgMarginSize(worksheet, 1, 2, 3);
```
```python
import vs

# Gets the worksheet cell's image margin size.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSImgMarginSize(worksheet, row, column)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
