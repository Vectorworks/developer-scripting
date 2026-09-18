# RemoveWSColumnOperator

## Description
Removes database column operator from specified column.

```pascal
PROCEDURE RemoveWSColumnOperator(
				worksheet    : HANDLE;
				databaseRow  : INTEGER;
				column       : INTEGER;
				operatorType : INTEGER);
```

```python
def vs.RemoveWSColumnOperator(worksheet, databaseRow, column, operatorType):
    return None
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
Summarize operator = 1<BR>
Add operator = 2

## Examples
```pascal
RemoveWSColumnOperator(worksheet, 1, 2, 3);
```
```python
import vs

# Removes database column operator from specified column.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
databaseRow = 10
column = 5
operatorType = 0

vs.RemoveWSColumnOperator(worksheet, databaseRow, column, operatorType)
```

## See Also
VS Functions:
* [AddWSColumnOperator](AddWSColumnOperator.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
