# SetupDialogC

## Description
A predefined constant value that is passed to the dialog event handler subroutine when a modern custom dialog is initially displayed onscreen.<BR>
<BR>
This constant is usually used to determine when to execute dialog initialization and setup calls.

```pascal
PROCEDURE SetupDialogC;
```

```python
def vs.SetupDialogC():
    return INTEGER
```

## Remarks
[DWD 1/20/00]

## Examples
```pascal
SetupDialogC;
```
```python
import vs

# A predefined constant value that is passed to the dialog event handler
# subroutine when a modern custom dialog is initially displayed onscreen.
resultN = vs.SetupDialogC()
vs.Message('SetupDialogC returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
