# GetWSImgUseLayScale

## Description
Determines if the image size type is Layer Scale.

```pascal
FUNCTION GetWSImgUseLayScale(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER): BOOLEAN;
```

```python
def vs.GetWSImgUseLayScale(worksheet, row, column):
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
resultOK := GetWSImgUseLayScale(worksheet, 1, 2);
```
```python
import vs

# Determines if the image size type is Layer Scale.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

ok = vs.GetWSImgUseLayScale(worksheet, row, column)
if ok:
    vs.Message('GetWSImgUseLayScale succeeded')
else:
    vs.Message('GetWSImgUseLayScale failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
