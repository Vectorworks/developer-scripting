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

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
