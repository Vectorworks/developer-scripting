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

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
