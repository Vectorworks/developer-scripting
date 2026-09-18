# GetWSCellTextAngle

## Description
Returns the text angle of a cell in the referenced worksheet

```pascal
PROCEDURE GetWSCellTextAngle(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER;
				VAR angle : INTEGER);
```

```python
def vs.GetWSCellTextAngle(worksheet, row, column):
    return angle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|row|INTEGER|Row of cell to be queried|
|column|INTEGER|Column of cell to be queried|
|angle|INTEGER|Text angle|

## Examples
```pascal
GetWSCellTextAngle(worksheet, 1, 2, 3);
```
```python
import vs

# Returns the text angle of a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSCellTextAngle(worksheet, row, column)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
