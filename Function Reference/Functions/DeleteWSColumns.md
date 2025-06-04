# DeleteWSColumns

## Description
Deletes columns from the referenced worksheet.

```pascal
PROCEDURE DeleteWSColumns(
				worksheet   : HANDLE;
				startColumn : INTEGER;
				numColumns  : INTEGER);
```

```python
def vs.DeleteWSColumns(worksheet, startColumn, numColumns):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|startColumn|INTEGER|Start column of delete operation.|
|numColumns|INTEGER|Number of columns to delete.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
