# SetWSCurrentCell

## Description
Sets the active cell of the referenced worksheet.

```pascal
PROCEDURE SetWSCurrentCell(
				worksheet         : HANDLE;
				currentCellRow    : INTEGER;
				currentCellColumn : INTEGER);
```

```python
def vs.SetWSCurrentCell(worksheet, currentCellRow, currentCellColumn):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|currentCellRow|INTEGER|Row of active cell.|
|currentCellColumn|INTEGER|Column of active cell.|

## Remarks
Sets the specified cell to be the worksheet's current cell. 
If specified cell is not contained within currently specified worksheet range, current selection is changed to single cell selection.

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
