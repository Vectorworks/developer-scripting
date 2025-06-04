# GetWSCellValue

## Description
Returns the displayed numeric value of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellValue(
				worksheet     : HANDLE;
				row           : INTEGER;
				column        : INTEGER;
				VAR cellValue : REAL);
```

```python
def vs.GetWSCellValue(worksheet, row, column):
    return cellValue
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|cellValue|REAL|Numeric value contained in worksheet cell.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
