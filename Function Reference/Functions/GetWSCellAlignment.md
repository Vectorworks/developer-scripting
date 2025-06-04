# GetWSCellAlignment

## Description
Returns the horizontal alignment setting of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellAlignment(
				worksheet         : HANDLE;
				row               : INTEGER;
				column            : INTEGER;
				VAR cellAlignment : INTEGER);
```

```python
def vs.GetWSCellAlignment(worksheet, row, column):
    return cellAlignment
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to a worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|cellAlignment|INTEGER|Horizontal alignment index of cell.|

## Remarks
Alignment constants:
General  = 0
Left         = 1
Center    = 2
Right      = 3

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
