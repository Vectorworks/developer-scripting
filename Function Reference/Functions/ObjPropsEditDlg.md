# ObjPropsEditDlg

## Description
Show object properties edit dialog.

```pascal
FUNCTION ObjPropsEditDlg(hObj : HANDLE): BOOLEAN;
```

```python
def vs.ObjPropsEditDlg(hObj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|The object which properties will be edited.|

## Examples
```pascal
resultOK := ObjPropsEditDlg(hObj);
```
```python
import vs

# Show object properties edit dialog.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.ObjPropsEditDlg(hObj)
if ok:
    vs.Message('ObjPropsEditDlg succeeded')
else:
    vs.Message('ObjPropsEditDlg failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Utility](../Categories/Utility.md)
