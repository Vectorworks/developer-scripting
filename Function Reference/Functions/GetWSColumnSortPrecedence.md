# GetWSColumnSortPrecedence

## Description
Gets database column sort precedence, if any.

```pascal
FUNCTION GetWSColumnSortPrecedence(
				worksheet   : HANDLE;
				databaseRow : INTEGER;
				column      : INTEGER): INTEGER;
```

```python
def vs.GetWSColumnSortPrecedence(worksheet, databaseRow, column):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|

## Examples
```pascal
resultN := GetWSColumnSortPrecedence(worksheet, 1, 2);
```
```python
import vs

# Gets database column sort precedence, if any.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
databaseRow = 10
column = 5

resultN = vs.GetWSColumnSortPrecedence(worksheet, databaseRow, column)
vs.Message('GetWSColumnSortPrecedence returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
