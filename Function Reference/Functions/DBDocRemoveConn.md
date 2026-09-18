# DBDocRemoveConn

## Description
Remove a database connection from the current document

```pascal
FUNCTION DBDocRemoveConn(databaseName : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBDocRemoveConn(databaseName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|databaseName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := DBDocRemoveConn(databaseName);
```
```python
import vs

# Remove a database connection from the current document.
databaseName = 'Example'

ok = vs.DBDocRemoveConn(databaseName)
if ok:
    vs.Message('DBDocRemoveConn succeeded')
else:
    vs.Message('DBDocRemoveConn failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
