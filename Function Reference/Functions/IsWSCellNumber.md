# IsWSCellNumber

## Description
Determines if a cell in the referenced worksheet contains a numeric value. The cell is referenced by its row-column position in the worksheet.

```pascal
FUNCTION IsWSCellNumber(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER): BOOLEAN;
```

```python
def vs.IsWSCellNumber(worksheet, row, column):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
