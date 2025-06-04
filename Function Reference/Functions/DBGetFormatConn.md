# DBGetFormatConn

## Description
Returns the ODBC connection for the specified format.

```pascal
FUNCTION DBGetFormatConn(
				formatName      : STRING;
				VAR outDatabase : STRING;
				VAR outTable    : STRING): BOOLEAN;
```

```python
def vs.DBGetFormatConn(formatName):
    return (BOOLEAN, outDatabase, outTable)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|formatName|STRING|   |
|outDatabase|STRING|   |
|outTable|STRING|   |

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
