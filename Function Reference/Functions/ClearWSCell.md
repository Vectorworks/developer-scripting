# ClearWSCell

## Description
Clears content and resets attributes of a cell in the referenced worksheet.

ClearWSCell allows a rectangular range of cells to be reset. To reset a single cell, specify identical values for the top/bottom and left/right range boundaries.

```pascal
PROCEDURE ClearWSCell(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER);
```

```python
def vs.ClearWSCell(worksheet, topRow, leftColumn, bottomRow, rightColumn):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|topRow|INTEGER|Top row of cell range.|
|leftColumn|INTEGER|Leftmost column of cell range.|
|bottomRow|INTEGER|Bottom row of cell range.|
|rightColumn|INTEGER|Rightmost column of cell range.|

## Examples
```pascal
BEGIN
	SetWSCellFormula (gClassWSHandle, 1+i, col+8, 1+i, col+8, gClassList [i].Description);
END
ELSE
	ClearWSCell (gClassWSHandle, 1+i, col+8, 1+i, col+8);
BEGIN
END;

BEGIN
ClearWSCell(kSchedFormatHand,1,1,(9 + kMaxNumSchedColumns), kMaxNumSchedules);
For SchedNum := 1 to kMaxNumSchedules DO
	BEGIN
		SetWSCellFormula(kSchedFormatHand,1, SchedNum,1, SchedNum, gScheduleNames[SchedNum]); {SchedName}
		SetWSCellFormula(kSchedFormatHand,2, SchedNum,2,SchedNum, gPrintedNames[SchedNum]); {printed Name}

{load the main heading}
SetWSCellFormula(tempHandle, 2, tempA, 2, tempA, Concat(' ', gSchFldInfo[tempA, 5]));
IF gSchFldInfo[tempA, 5] = kDash THEN ClearWSCell(tempHandle, 2, tempA, 2, tempA);
```
```python
import vs

# Clears content and resets attributes of a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5

vs.ClearWSCell(worksheet, topRow, leftColumn, bottomRow, rightColumn)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
