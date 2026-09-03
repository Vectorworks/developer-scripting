# DidCancel

## Description
Function DidCancel detects whether the Cancel button in a predefined dialog was pressed. DidCancel is intended for use with conditional statements to signal that a cancel event has occurred.

```pascal
FUNCTION DidCancel : BOOLEAN;
```

```python
def vs.DidCancel():
    return BOOLEAN
```

## Examples
[SimpleDialog](examples/SimpleDialog.md)

```pascal
resultOK := DidCancel;
```
```python
import vs

# Function DidCancel detects whether the Cancel button in a predefined dialog
# was pressed.
ok = vs.DidCancel()
if ok:
    vs.Message('DidCancel succeeded')
else:
    vs.Message('DidCancel failed')
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
