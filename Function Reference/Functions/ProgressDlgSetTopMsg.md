# ProgressDlgSetTopMsg

## Description
Set top message of a progress dialog.

```pascal
PROCEDURE ProgressDlgSetTopMsg(message : STRING);
```

```python
def vs.ProgressDlgSetTopMsg(message):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|STRING|   |

## Examples
les can be found at [[VS:Progress Dialog]].

```pascal
ProgressDlgSetTopMsg('Example');
```
```python
import vs

# Set top message of a progress dialog.
message = 'Hello Vectorworks'

vs.ProgressDlgSetTopMsg(message)
```

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
