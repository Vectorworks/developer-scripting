# DBSQLExecuteGet

## Description
Retrieves information from the resultSetInstance created with 'DBSQLExecute' or 'DBSQLExecuteDSN'

```pascal
FUNCTION DBSQLExecuteGet(
				resultSetInst     : LONGINT;
				colIndex          : LONGINT;
				VAR outColumnName : DYNARRAY[] of CHAR;
				VAR outValue      : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBSQLExecuteGet(resultSetInst, colIndex):
    return (BOOLEAN, outColumnName, outValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|resultSetInst|LONGINT|   |
|colIndex|LONGINT|   |
|outColumnName|DYNARRAY[] of CHAR|   |
|outValue|DYNARRAY[] of CHAR|   |

## Examples
[[VS:DBSQLExecuteDSN]]

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
