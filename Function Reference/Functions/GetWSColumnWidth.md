# GetWSColumnWidth

## Description
Returns the width of a column in the referenced worksheet.

```pascal
PROCEDURE GetWSColumnWidth(
				worksheet : HANDLE;
				column    : INTEGER;
				VAR width : INTEGER);
```

```python
def vs.GetWSColumnWidth(worksheet, column):
    return width
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|column|INTEGER|Column to be queried.|
|width|INTEGER|Width of column (in pixels).|

## Examples
```pascal
GetWSColumnWidth(worksheet, 1, 2);
```
```python
import vs

# Returns the width of a column in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
column = 5

result = vs.GetWSColumnWidth(worksheet, column)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
