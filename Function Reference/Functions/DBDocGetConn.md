# DBDocGetConn

## Description
Get database connection info.

```pascal
FUNCTION DBDocGetConn(
				databaseName    : DYNARRAY[] of CHAR;
				VAR outUserName : DYNARRAY[] of CHAR;
				VAR outPassword : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBDocGetConn(databaseName):
    return (BOOLEAN, outUserName, outPassword)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|databaseName|DYNARRAY[] of CHAR|   |
|outUserName|DYNARRAY[] of CHAR|   |
|outPassword|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := DBDocGetConn(databaseName, outUserName, outPassword);
```
```python
import vs

# Get database connection info.
databaseName = 'Example'

ok, outUserName, outPassword = vs.DBDocGetConn(databaseName)
vs.Message('DBDocGetConn returned: ' + str((ok, outUserName, outPassword)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
