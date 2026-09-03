# GetWSCellWrapTextFlag

## Description
Returns the wrap text state of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellWrapTextFlag(
				worksheet        : HANDLE;
				row              : INTEGER;
				column           : INTEGER;
				VAR wrapTextFlag : BOOLEAN);
```

```python
def vs.GetWSCellWrapTextFlag(worksheet, row, column):
    return wrapTextFlag
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|row|INTEGER|Row of cell to be queried|
|column|INTEGER|Row of cell to be queried|
|wrapTextFlag|BOOLEAN|Wrap text flag|

## Examples
```pascal
GetWSCellWrapTextFlag(worksheet, 1, 2, TRUE);
```
```python
import vs

# Returns the wrap text state of a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

result = vs.GetWSCellWrapTextFlag(worksheet, row, column)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
