# GetWSRowHeight

## Description
Returns the height of a row in the referenced worksheet.

```pascal
PROCEDURE GetWSRowHeight(
				worksheet  : HANDLE;
				row        : INTEGER;
				VAR height : INTEGER);
```

```python
def vs.GetWSRowHeight(worksheet, row):
    return height
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row to be queried.|
|height|INTEGER|Height of row (in pixels).|

## Examples
```pascal
GetWSRowHeight(worksheet, 1, 2);
```
```python
import vs

# Returns the height of a row in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10

result = vs.GetWSRowHeight(worksheet, row)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
