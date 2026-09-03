# DBDocSetColKey

## Description
Set database table column to be as a key.

```pascal
FUNCTION DBDocSetColKey(
				databaseName : DYNARRAY[] of CHAR;
				tableName    : DYNARRAY[] of CHAR;
				columnName   : DYNARRAY[] of CHAR;
				setIsKey     : BOOLEAN): BOOLEAN;
```

```python
def vs.DBDocSetColKey(databaseName, tableName, columnName, setIsKey):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|databaseName|DYNARRAY[] of CHAR|Data source name.|
|tableName|DYNARRAY[] of CHAR|Table name.|
|columnName|DYNARRAY[] of CHAR|Column name.|
|setIsKey|BOOLEAN|Set TRUE if this column to be used as key in WHERE clauses.|

## Examples
```pascal
resultOK := DBDocSetColKey(databaseName, tableName, columnName, TRUE);
```
```python
import vs

# Set database table column to be as a key.
databaseName = 'Example'
tableName = 'Example'
columnName = 'Example'
setIsKey = True

ok = vs.DBDocSetColKey(databaseName, tableName, columnName, setIsKey)
if ok:
    vs.Message('DBDocSetColKey succeeded')
else:
    vs.Message('DBDocSetColKey failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
