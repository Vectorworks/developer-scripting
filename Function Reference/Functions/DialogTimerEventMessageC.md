# DialogTimerEventMessageC

## Description
This constant represents the message that is sent periodically to a dialog handler after it has been registered to receive timer events.

```pascal
PROCEDURE DialogTimerEventMessageC;
```

```python
def vs.DialogTimerEventMessageC():
    return INTEGER
```

## Examples
```pascal
DialogTimerEventMessageC;
```
```python
import vs

# This constant represents the message that is sent periodically to a dialog
# handler after it has been registered to receive timer events.
resultN = vs.DialogTimerEventMessageC()
vs.Message('DialogTimerEventMessageC returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
