# GetWSCellBorder

## Description
Returns the cell border of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellBorder(
				worksheet  : HANDLE;
				row        : INTEGER;
				column     : INTEGER;
				VAR top    : BOOLEAN;
				VAR left   : BOOLEAN;
				VAR bottom : BOOLEAN;
				VAR right  : BOOLEAN);
```

```python
def vs.GetWSCellBorder(worksheet, row, column):
    return (top, left, bottom, right)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|top|BOOLEAN|Top border ON-OFF status.|
|left|BOOLEAN|Left border ON-OFF status.|
|bottom|BOOLEAN|Bottom border ON-OFF status.|
|right|BOOLEAN|Right border ON-OFF status.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
