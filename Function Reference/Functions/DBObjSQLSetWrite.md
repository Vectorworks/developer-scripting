# DBObjSQLSetWrite

## Description
Set an object's SQL query for ODBC write.

This SQL query writes to database, so the query should be an UPDATE query, e.g.

'''UPDATE''' [Columns] '''SET''' [Center Mark Size]=0.5 '''WHERE''' [ID]=1

```pascal
FUNCTION DBObjSQLSetWrite(
				hRecord     : HANDLE;
				SQLSentence : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBObjSQLSetWrite(hRecord, SQLSentence):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hRecord|HANDLE|The handle to linked record.|
|SQLSentence|DYNARRAY[] of CHAR|The UPDATE query.|

## Examples
```pascal
resultOK := DBObjSQLSetWrite(hRecord, SQLSentence);
```
```python
import vs

# Set an object's SQL query for ODBC write.
hRecord = vs.GetObject('MyRecord')  # handle to a record format
SQLSentence = 'Example'

ok = vs.DBObjSQLSetWrite(hRecord, SQLSentence)
if ok:
    vs.Message('DBObjSQLSetWrite succeeded')
else:
    vs.Message('DBObjSQLSetWrite failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
