# DisplayDialogHelpC

## Description
This constant is passed to the event handler routine to signal the dialog that it should display its contextual help using the help string given by the Contextual Help Manager menu.

```pascal
PROCEDURE DisplayDialogHelpC;
```

```python
def vs.DisplayDialogHelpC():
    return INTEGER
```

## Remarks
Added 2/09/2007 by Lyndsey Ferguson

## Examples
```pascal
DisplayDialogHelpC;
```
```python
import vs

# This constant is passed to the event handler routine to signal the dialog
# that it should display its contextual help using the help string given by
# the Conte.
resultN = vs.DisplayDialogHelpC()
vs.Message('DisplayDialogHelpC returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
