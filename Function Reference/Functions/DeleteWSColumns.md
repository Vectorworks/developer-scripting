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

## Examples
```pascal
BEGIN
AddCol := Abs(AddCol);
DeleteWSColumns(WSHand,1,AddCol);
END;

BEGIN
AddCol := Abs(AddCol);
DeleteWSColumns(gInventoryReportHan,1,AddCol);
END;
```
```python
import vs

# Deletes columns from the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
startColumn = 5
numColumns = 5

vs.DeleteWSColumns(worksheet, startColumn, numColumns)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
