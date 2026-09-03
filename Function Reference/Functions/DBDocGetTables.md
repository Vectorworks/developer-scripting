# DBDocGetTables

## Description
Returns a string representing a ';' delimited list of the tables in the specified database.

```pascal
FUNCTION DBDocGetTables(
				database      : STRING;
				VAR outTables : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBDocGetTables(database):
    return (BOOLEAN, outTables)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|database|STRING|   |
|outTables|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := DBDocGetTables('Example', outTables);
```
```python
import vs

# Returns a string representing a ';' delimited list of the tables in the
# specified database.
database = 'Example'

ok, outTables = vs.DBDocGetTables(database)
vs.Message('DBDocGetTables returned: ' + str((ok, outTables)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
