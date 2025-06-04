# GetWSCellFormula

## Description
Returns the formula from a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellFormula(
				worksheet   : HANDLE;
				row         : INTEGER;
				column      : INTEGER;
				VAR formula : STRING);
```

```python
def vs.GetWSCellFormula(worksheet, row, column):
    return formula
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|formula|STRING|Formula contained in worksheet cell.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
