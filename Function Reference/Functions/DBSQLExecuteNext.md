# DBSQLExecuteNext

## Description
Moves the resultSet current pointer to the next entry.

```pascal
FUNCTION DBSQLExecuteNext(resultSetInst : LONGINT): BOOLEAN;
```

```python
def vs.DBSQLExecuteNext(resultSetInst):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|resultSetInst|LONGINT|   |

## Examples
[DBSQLExecuteDSN](DBSQLExecuteDSN.md)

```pascal
resultOK := DBSQLExecuteNext(1);
```
```python
import vs

# Moves the resultSet current pointer to the next entry.
resultSetInst = 1

ok = vs.DBSQLExecuteNext(resultSetInst)
if ok:
    vs.Message('DBSQLExecuteNext succeeded')
else:
    vs.Message('DBSQLExecuteNext failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
