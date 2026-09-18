# MoveWSColumnOperator

## Description
Moves database column operator between columns.

```pascal
PROCEDURE MoveWSColumnOperator(
				worksheet    : HANDLE;
				databaseRow  : INTEGER;
				fromColumn   : INTEGER;
				toColumn     : INTEGER;
				operatorType : INTEGER);
```

```python
def vs.MoveWSColumnOperator(worksheet, databaseRow, fromColumn, toColumn, operatorType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Database row to be queried.|
|fromColumn|INTEGER|From column to be queried.|
|toColumn|INTEGER|To column to be queried.|
|operatorType|INTEGER|Operator type.|

## Remarks
Operator type constants:<BR>
All operators = -1<BR>
Sort operator = 0<BR>
Summarize operatory = 1

## Examples
```pascal
MoveWSColumnOperator(worksheet, 1, 2, 3, 10);
```
```python
import vs

# Moves database column operator between columns.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
databaseRow = 10
fromColumn = 5
toColumn = 5
operatorType = 0

vs.MoveWSColumnOperator(worksheet, databaseRow, fromColumn, toColumn, operatorType)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
