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

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
