# ResizeDialogC

## Description
This constant is passed to the event handler routine to signal the dialog has been resized.

```pascal
PROCEDURE ResizeDialogC;
```

```python
def vs.ResizeDialogC():
    return INTEGER
```

## Remarks
Added 1/7/05 by Jeff Geraci.

## Examples
```pascal
ResizeDialogC;
```
```python
import vs

# This constant is passed to the event handler routine to signal the dialog
# has been resized.
resultN = vs.ResizeDialogC()
vs.Message('ResizeDialogC returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
