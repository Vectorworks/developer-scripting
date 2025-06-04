# SetWSSelection

## Description
Sets the current selection range of the referenced worksheet.

In addition to setting the selection range of a worksheet, SetWSSelection will can also set the selection range of database subrows, where applicable.

```pascal
PROCEDURE SetWSSelection(
				worksheet         : HANDLE;
				currentCellRow    : INTEGER;
				currentCellColumn : INTEGER;
				topRangeRow       : INTEGER;
				leftRangeColumn   : INTEGER;
				topRangeSubrow    : INTEGER;
				bottomRangeRow    : INTEGER;
				rightRangeColumn  : INTEGER;
				bottomRangeSubrow : INTEGER);
```

```python
def vs.SetWSSelection(worksheet, currentCellRow, currentCellColumn, topRangeRow, leftRangeColumn, topRangeSubrow, bottomRangeRow, rightRangeColumn, bottomRangeSubrow):
    return None
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
