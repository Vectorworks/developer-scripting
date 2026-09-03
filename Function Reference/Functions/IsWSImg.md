# IsWSImg

## Description
Determines if worksheet cell is set to display an image.

```pascal
FUNCTION IsWSImg(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER): BOOLEAN;
```

```python
def vs.IsWSImg(worksheet, row, column):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|

## Examples
```pascal
resultOK := IsWSImg(worksheet, 1, 2);
```
```python
import vs

# Determines if worksheet cell is set to display an image.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

ok = vs.IsWSImg(worksheet, row, column)
if ok:
    vs.Message('IsWSImg succeeded')
else:
    vs.Message('IsWSImg failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
