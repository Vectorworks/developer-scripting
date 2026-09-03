# NonUndoableActionOK

## Description
Function NonUndoableActionOK displays a dialog informing the user that the action that is about to be performed cannot be undone. If the user selects OK, the function returns TRUE. If the &quot;Show Undo Warnings&quot; preference is turned off, this function just returns TRUE and does not display a dialog.

```pascal
FUNCTION NonUndoableActionOK : BOOLEAN;
```

```python
def vs.NonUndoableActionOK():
    return BOOLEAN
```

## Examples
```pascal
resultOK := NonUndoableActionOK;
```
```python
import vs

# Function NonUndoableActionOK displays a dialog informing the user that the
# action that is about to be performed cannot be undone.
ok = vs.NonUndoableActionOK()
if ok:
    vs.Message('NonUndoableActionOK succeeded')
else:
    vs.Message('NonUndoableActionOK failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
