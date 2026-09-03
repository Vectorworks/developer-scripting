# DBDocHasConn

## Description
Checks if the current document has connections to an ODBC data source.

```pascal
FUNCTION DBDocHasConn : BOOLEAN;
```

```python
def vs.DBDocHasConn():
    return BOOLEAN
```

## Examples
```pascal
resultOK := DBDocHasConn;
```
```python
import vs

# Checks if the current document has connections to an ODBC data source.
ok = vs.DBDocHasConn()
if ok:
    vs.Message('DBDocHasConn succeeded')
else:
    vs.Message('DBDocHasConn failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
