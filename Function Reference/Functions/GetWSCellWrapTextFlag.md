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

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
