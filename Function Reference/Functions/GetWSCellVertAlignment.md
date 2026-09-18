# GetWSCellVertAlignment

## Description
Returns the vertical alignment setting of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellVertAlignment(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				VAR vAlignment : INTEGER);
```

```python
def vs.GetWSCellVertAlignment(worksheet, row, column):
    return vAlignment
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|row|INTEGER|Row index of cell to be queried|
|column|INTEGER|Column index of cell to be queried|
|vAlignment|INTEGER|Vertical alignment index of cell.|

## Remarks
Vertical alignment constants:
top = 1
center  = 3
bottom = 5

## Examples
```pascal
GetWSCellVertAlignment(worksheet, 1, 2, 3);
```
```python
import vs

# Returns the vertical alignment setting of a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSCellVertAlignment(worksheet, row, column)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
