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

## Examples
```pascal
resultOK := DBObjSQLGetWrite(hRecord, SQLSentence);
```
```python
import vs

# Get an object's SQL sentence for ODBC write.
hRecord = vs.GetObject('MyRecord')  # handle to a record format

ok, SQLSentence = vs.DBObjSQLGetWrite(hRecord)
vs.Message('DBObjSQLGetWrite returned: ' + str((ok, SQLSentence)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
