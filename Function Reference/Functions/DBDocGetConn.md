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

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
