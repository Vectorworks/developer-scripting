# SetdownDialogC

## Description
A predefined constant value that is passed to the dialog event handler subroutine when a modern custom dialog is dismissed.<BR>
<BR>
This constant is usually used to determine when to execute dialog cleanup calls prior to exiting the dialog.

```pascal
PROCEDURE SetdownDialogC;
```

```python
def vs.SetdownDialogC():
    return INTEGER
```

## Remarks
[DWD 1/20/00]

## Examples
```pascal
SetdownDialogC;
```
```python
import vs

# A predefined constant value that is passed to the dialog event handler
# subroutine when a modern custom dialog is dismissed.
resultN = vs.SetdownDialogC()
vs.Message('SetdownDialogC returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetupDialogC](SetupDialogC.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
