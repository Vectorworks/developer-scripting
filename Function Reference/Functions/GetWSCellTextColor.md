# GetWSCellTextColor

## Description
Returns the text color of a cell in the referenced worksheet

```pascal
PROCEDURE GetWSCellTextColor(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER;
				VAR color : LONGINT);
```

```python
def vs.GetWSCellTextColor(worksheet, row, column):
    return color
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|row|INTEGER|Row of cell to be queried|
|column|INTEGER|Column of cell to be queried|
|color|LONGINT|Text color index value|

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
