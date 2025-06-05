# DBSQLExecute

## Description
Executes a SQL in the specified database connected to the current document. Note! The resultSetInstance have to be deleted with call to 'DBSQLExecuteDelete'

```pascal
FUNCTION DBSQLExecute(
				database             : STRING;
				SQLQuery             : DYNARRAY[] of CHAR;
				VAR outColumnCnt     : LONGINT;
				VAR outResultSetInst : LONGINT): BOOLEAN;
```

```python
def vs.DBSQLExecute(database, SQLQuery):
    return (BOOLEAN, outColumnCnt, outResultSetInst)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|database|STRING|   |
|SQLQuery|DYNARRAY[] of CHAR|   |
|outColumnCnt|LONGINT|   |
|outResultSetInst|LONGINT|   |

## Examples
[DBSQL](examples/DBSQL.md)

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
