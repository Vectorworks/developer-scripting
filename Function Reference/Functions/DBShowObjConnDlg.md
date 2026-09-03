# DBShowObjConnDlg

## Description
Show the object connection dialog for the selected objects.

```pascal
FUNCTION DBShowObjConnDlg : BOOLEAN;
```

```python
def vs.DBShowObjConnDlg():
    return BOOLEAN
```

## Examples
```pascal
resultOK := DBShowObjConnDlg;
```
```python
import vs

# Show the object connection dialog for the selected objects.
ok = vs.DBShowObjConnDlg()
if ok:
    vs.Message('DBShowObjConnDlg succeeded')
else:
    vs.Message('DBShowObjConnDlg failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
