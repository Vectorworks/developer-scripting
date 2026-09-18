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

## Examples
```pascal
SetWSSelection(worksheet, 1, 2, 3, 10, 5, 1, 2, 3);
```
```python
import vs

# Sets the current selection range of the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
currentCellRow = 10
currentCellColumn = 5
topRangeRow = 10
leftRangeColumn = 5
topRangeSubrow = 10
bottomRangeRow = 10
rightRangeColumn = 5
bottomRangeSubrow = 10

vs.SetWSSelection(worksheet, currentCellRow, currentCellColumn, topRangeRow, leftRangeColumn, topRangeSubrow, bottomRangeRow, rightRangeColumn, bottomRangeSubrow)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
