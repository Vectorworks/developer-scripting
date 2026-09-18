# GetWSImgView

## Description
Gets the specified worksheet cell's image view.

```pascal
PROCEDURE GetWSImgView(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER;
				VAR view  : INTEGER);
```

```python
def vs.GetWSImgView(worksheet, row, column):
    return view
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|view|INTEGER|The image view.|

## Examples
```pascal
GetWSImgView(worksheet, 1, 2, 3);
```
```python
import vs

# Gets the specified worksheet cell's image view.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSImgView(worksheet, row, column)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Worksheets](../Categories/Worksheets.md)
