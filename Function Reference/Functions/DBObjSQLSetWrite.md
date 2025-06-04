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

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
