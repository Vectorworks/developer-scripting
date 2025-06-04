# DeleteWSRows

## Description
Deletes rows from the referenced worksheet.

```pascal
PROCEDURE DeleteWSRows(
				worksheet : HANDLE;
				startRow  : INTEGER;
				numRows   : INTEGER);
```

```python
def vs.DeleteWSRows(worksheet, startRow, numRows):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|startRow|INTEGER|Start row of delete operation.|
|numRows|INTEGER|Number of rows to be deleted.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
