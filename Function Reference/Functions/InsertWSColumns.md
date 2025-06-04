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

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
