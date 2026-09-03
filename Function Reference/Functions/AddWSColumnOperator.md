# AddWSColumnOperator

## Description
Adds database column operator to specified column.

```pascal
PROCEDURE AddWSColumnOperator(
				worksheet    : HANDLE;
				databaseRow  : INTEGER;
				column       : INTEGER;
				operatorType : INTEGER);
```

```python
def vs.AddWSColumnOperator(worksheet, databaseRow, column, operatorType):
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
AddWSColumnOperator(worksheet, 1, 2, 3);
```
```python
import vs

# Adds database column operator to specified column.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
databaseRow = 10
column = 5
operatorType = 0

vs.AddWSColumnOperator(worksheet, databaseRow, column, operatorType)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
