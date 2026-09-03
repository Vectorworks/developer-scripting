# ProgressDlgHasCancel

## Description
Determine if the dialog has been canceled. The dialog must have cancelation enabled when created.

```pascal
FUNCTION ProgressDlgHasCancel : BOOLEAN;
```

```python
def vs.ProgressDlgHasCancel():
    return BOOLEAN
```

## Examples
les can be found at [[VS:Progress Dialog]].

```pascal
resultOK := ProgressDlgHasCancel;
```
```python
import vs

# Determine if the dialog has been canceled.
ok = vs.ProgressDlgHasCancel()
if ok:
    vs.Message('ProgressDlgHasCancel succeeded')
else:
    vs.Message('ProgressDlgHasCancel failed')
```

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
