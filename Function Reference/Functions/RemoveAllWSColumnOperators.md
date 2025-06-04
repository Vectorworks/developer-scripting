# RemoveAllWSColumnOperators

## Description
Removes all database column operators from specified database row.

```pascal
PROCEDURE RemoveAllWSColumnOperators(
				worksheet    : HANDLE;
				databaseRow  : INTEGER;
				operatorType : INTEGER);
```

```python
def vs.RemoveAllWSColumnOperators(worksheet, databaseRow, operatorType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Database row to be queried.|
|operatorType|INTEGER|Operator type.|

## Remarks
Operator type constants:<BR>
All operators = -1<BR>
Sort operator = 0<BR>
Summarize operatory = 1

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
