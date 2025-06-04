# SetWSColumnSortType

## Description
Sets database column sort type.

```pascal
PROCEDURE SetWSColumnSortType(
				worksheet   : HANDLE;
				databaseRow : INTEGER;
				column      : INTEGER;
				sortType    : INTEGER);
```

```python
def vs.SetWSColumnSortType(worksheet, databaseRow, column, sortType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|
|sortType|INTEGER|   |

## Remarks
Sort type constants:<BR>
Sort ascending = 0<BR>
Sort descending = 1

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
