# DBObjSQLGetWrite

## Description
Get an object's SQL sentence for ODBC write.

```pascal
FUNCTION DBObjSQLGetWrite(
				hRecord         : HANDLE;
				VAR SQLSentence : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.DBObjSQLGetWrite(hRecord):
    return (BOOLEAN, SQLSentence)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hRecord|HANDLE|   |
|SQLSentence|DYNARRAY[] of CHAR|   |

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
