# ProgressDlgEnd

## Description
End a progress context started with ProgressDlgStart. This will make the progress jump to the percentage declared when started.

```pascal
PROCEDURE ProgressDlgEnd;
```

```python
def vs.ProgressDlgEnd():
    return None
```

## Examples
les can be found at [[VS:Progress Dialog]].

```pascal
ProgressDlgEnd;
```
```python
import vs

# End a progress context started with ProgressDlgStart.
vs.ProgressDlgEnd()
```

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
