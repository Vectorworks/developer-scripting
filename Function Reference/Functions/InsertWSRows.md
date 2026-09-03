# InsertWSRows

## Description
Inserts rows into a referenced worksheet.

```pascal
PROCEDURE InsertWSRows(
				worksheet : HANDLE;
				beforeRow : INTEGER;
				numRows   : INTEGER);
```

```python
def vs.InsertWSRows(worksheet, beforeRow, numRows):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|beforeRow|INTEGER|Insert location for new worksheet rows.|
|numRows|INTEGER|Number of rows to insert.|

## Examples
```pascal
wsHand := GetObject(wsName);
if wsHand <> nil then BEGIN
	if GetType(wsHand) = 18 then BEGIN
		GetWSRowColumnCount(wsHand, numRows, numCols);
		IF numRows < kNumRows THEN InsertWSRows   (wsHand, 1, kNumRows - numRows);
		IF numCols < kNumCols THEN InsertWSColumns(wsHand, 1, kNumCols - numCols);
	end else BEGIN
		while GetObject(wsName) <> nil DO wsName := Concat(wsName, '-1');
		wsHand := NIL;

BEGIN
	InsertWSRows (wksH2, nRows, numGridPoints + 5 - nRows);
	SetWSCellNumberFormat(wksH2, nRows - 1, 1, numGridPoints + 5, 6, 13, 0, '', '');
END;

BEGIN
InsertWSRows(WSHand,1,AddRows);
END
```
```python
import vs

# Inserts rows into a referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
beforeRow = 10
numRows = 5

vs.InsertWSRows(worksheet, beforeRow, numRows)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
