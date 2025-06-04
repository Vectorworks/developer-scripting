# DBObjSQLSetRead

## Description
Set an object's SQL query for ODBC read.

This SQL query is used to update the Vectorworks document, so the query should be an SELECT query, e.g.

'''SELECT''' [ID],[Center Mark Size],[Use Center Marks],[Height],[Struct Width],[Struct Depth] '''FROM''' [Columns] '''WHERE''' [ID]=1

```pascal
FUNCTION DBObjSQLSetRead(
				hRecord     : HANDLE;
				SQLSentence : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBObjSQLSetRead(hRecord, SQLSentence):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hRecord|HANDLE|The handle to linked record.|
|SQLSentence|DYNARRAY[] of CHAR|The SELECT query.|

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
