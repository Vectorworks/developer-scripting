# DBSQLExecuteDSN

## Description
Executes a SQL query the specified DSN. It is not necessary to be registered in the ODBC manager. '''Note!''' The resultSetInstance have to be deleted with call to [DBSQLExecuteDelete](DBSQLExecuteDelete.md)

```pascal
FUNCTION DBSQLExecuteDSN(
				dsn                  : DYNARRAY[] of CHAR;
				userName             : DYNARRAY[] of CHAR;
				password             : DYNARRAY[] of CHAR;
				SQLQuery             : DYNARRAY[] of CHAR;
				VAR outColumnCnt     : LONGINT;
				VAR outResultSetInst : LONGINT): BOOLEAN;
```

```python
def vs.DBSQLExecuteDSN(dsn, userName, password, SQLQuery):
    return (BOOLEAN, outColumnCnt, outResultSetInst)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dsn|DYNARRAY[] of CHAR|   |
|userName|DYNARRAY[] of CHAR|   |
|password|DYNARRAY[] of CHAR|   |
|SQLQuery|DYNARRAY[] of CHAR|   |
|outColumnCnt|LONGINT|   |
|outResultSetInst|LONGINT|   |

## Remarks
CMP: DSN param appears to need a POSIX path

## Examples
[DBSQL](examples/DBSQL.md)

## See Also
[DBSQLExecuteGet](DBSQLExecuteGet.md) | [DBSQLExecuteNext](DBSQLExecuteNext.md) | [DBSQLExecuteDelete](DBSQLExecuteDelete.md)

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
