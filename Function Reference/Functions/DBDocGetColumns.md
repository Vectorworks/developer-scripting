# DBDocGetColumns

## Description
Returns a string representing a ';' delimited lists of the specified table data.

```pascal
FUNCTION DBDocGetColumns(
				database        : STRING;
				table           : STRING;
				VAR outNames    : DYNARRAY[] of CHAR;
				VAR outTypes    : DYNARRAY[] of CHAR;
				VAR outCanBeKey : DYNARRAY[] of CHAR;
				VAR outIsKey    : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBDocGetColumns(database, table):
    return (BOOLEAN, outNames, outTypes, outCanBeKey, outIsKey)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|database|STRING|   |
|table|STRING|   |
|outNames|DYNARRAY[] of CHAR|   |
|outTypes|DYNARRAY[] of CHAR|   |
|outCanBeKey|DYNARRAY[] of CHAR|   |
|outIsKey|DYNARRAY[] of CHAR|   |

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
