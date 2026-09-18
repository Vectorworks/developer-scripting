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

## Examples
```pascal
CASE gFindMode OF
1:	BEGIN
		ShowWS( WSh, TRUE );
		SetTopVisibleWS( WSh );
		SetWSCurrentCell(WSh, row, col);
		ProcessFoundCell := TRUE;
	END;

	SetWSCellAlignment(SymbolListWS,2,2,SymCounter+2,kMaxMotorFields,2);
	SetWSColumnWidth(SymbolListWS,2,kMaxMotorFields,90);
	ShowWS(SymbolListWS,TRUE);
	SetWSCurrentCell(SymbolListWS,SymCounter+3,1);
END; {PROCEDURE FillWorksheet}
```
```python
import vs

# Sets the active cell of the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
currentCellRow = 10
currentCellColumn = 5

vs.SetWSCurrentCell(worksheet, currentCellRow, currentCellColumn)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
