# HasWSColumnOperator

## Description
Determines if specified column operator is set in column.

```pascal
FUNCTION HasWSColumnOperator(
				worksheet    : HANDLE;
				databaseRow  : INTEGER;
				column       : INTEGER;
				operatorType : INTEGER): BOOLEAN;
```

```python
def vs.HasWSColumnOperator(worksheet, databaseRow, column, operatorType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|
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
