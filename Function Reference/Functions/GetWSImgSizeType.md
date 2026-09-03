# GetWSImgSizeType

## Description
Gets the worksheet cell's image size type.

```pascal
FUNCTION GetWSImgSizeType(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER): INTEGER;
```

```python
def vs.GetWSImgSizeType(worksheet, row, column):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|

## Remarks
* 0 = AutoSize size
* 1 = Fixed size
* 2 = Scale size

## Examples
```pascal
resultN := GetWSImgSizeType(worksheet, 1, 2);
```
```python
import vs

# Gets the worksheet cell's image size type.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

resultN = vs.GetWSImgSizeType(worksheet, row, column)
vs.Message('GetWSImgSizeType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
