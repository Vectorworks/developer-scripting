# InsertWSColumns

## Description
Inserts columns into the referenced worksheet.

```pascal
PROCEDURE InsertWSColumns(
				worksheet    : HANDLE;
				beforeColumn : INTEGER;
				numColumns   : INTEGER);
```

```python
def vs.InsertWSColumns(worksheet, beforeColumn, numColumns):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|beforeColumn|INTEGER|Insert location of new columns.|
|numColumns|INTEGER|Number of columns to insert.|

## Examples
```pascal
if wsHand <> nil then BEGIN
	if GetType(wsHand) = 18 then BEGIN
		GetWSRowColumnCount(wsHand, numRows, numCols);
		IF numRows < kNumRows THEN InsertWSRows   (wsHand, 1, kNumRows - numRows);
		IF numCols < kNumCols THEN InsertWSColumns(wsHand, 1, kNumCols - numCols);
	end else BEGIN
		while GetObject(wsName) <> nil DO wsName := Concat(wsName, '-1');
		wsHand := NIL;
	END;

BEGIN
InsertWSColumns(WSHand,1,AddCol);
END

BEGIN
InsertWSColumns(gInventoryReportHan,1,AddCol);
END
```
```python
import vs

# Inserts columns into the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
beforeColumn = 5
numColumns = 5

vs.InsertWSColumns(worksheet, beforeColumn, numColumns)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
