# GetWSColumnSortType

## Description
Gets database column's sort type.

```pascal
FUNCTION GetWSColumnSortType(
				worksheet   : HANDLE;
				databaseRow : INTEGER;
				column      : INTEGER): INTEGER;
```

```python
def vs.GetWSColumnSortType(worksheet, databaseRow, column):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|

## Remarks
Sort type constants:<BR>
Sort ascending = 0<BR>
Sort descending = 1

## Examples
```pascal
resultN := GetWSColumnSortType(worksheet, 1, 2);
```
```python
import vs

# Gets database column's sort type.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
databaseRow = 10
column = 5

resultN = vs.GetWSColumnSortType(worksheet, databaseRow, column)
vs.Message('GetWSColumnSortType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
