# GetWSImgUseObjectImg

## Description
Determines if cell uses object image.

```pascal
FUNCTION GetWSImgUseObjectImg(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER): BOOLEAN;
```

```python
def vs.GetWSImgUseObjectImg(worksheet, row, column):
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
resultOK := GetWSImgUseObjectImg(worksheet, 1, 2);
```
```python
import vs

# Determines if cell uses object image.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

ok = vs.GetWSImgUseObjectImg(worksheet, row, column)
if ok:
    vs.Message('GetWSImgUseObjectImg succeeded')
else:
    vs.Message('GetWSImgUseObjectImg failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
