# GetWSSelection

## Description
Returns the current selection range of the referenced worksheet.

In addition to returning the selection range of a worksheet, GetWSSelection will also return the range of selected database subrows, where applicable.

```pascal
PROCEDURE GetWSSelection(
				worksheet             : HANDLE;
				VAR currentCellRow    : INTEGER;
				VAR currentCellColumn : INTEGER;
				VAR topRangeRow       : INTEGER;
				VAR leftRangeColumn   : INTEGER;
				VAR topRangeSubrow    : INTEGER;
				VAR bottomRangeRow    : INTEGER;
				VAR rightRangeColumn  : INTEGER;
				VAR bottomRangeSubrow : INTEGER);
```

```python
def vs.GetWSSelection(worksheet):
    return (currentCellRow, currentCellColumn, topRangeRow, leftRangeColumn, topRangeSubrow, bottomRangeRow, rightRangeColumn, bottomRangeSubrow)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|currentCellRow|INTEGER|Row of currently active cell.|
|currentCellColumn|INTEGER|Column of currently active cell.|
|topRangeRow|INTEGER|Top row of selection range.|
|leftRangeColumn|INTEGER|Leftmost column of selection range.|
|topRangeSubrow|INTEGER|Top row of of subrow selection range.|
|bottomRangeRow|INTEGER|Bottom row of selection range.|
|rightRangeColumn|INTEGER|Rightmost column of selection range.|
|bottomRangeSubrow|INTEGER|Bottom row of subrow selection range.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
