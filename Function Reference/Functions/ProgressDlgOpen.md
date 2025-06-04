# ProgressDlgOpen

## Description
Show a progress dialog that doesn't interrupt the script. ProgressDlgClose must be used to close the dialog.

```pascal
PROCEDURE ProgressDlgOpen(
				title     : STRING;
				canCancel : BOOLEAN);
```

```python
def vs.ProgressDlgOpen(title, canCancel):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|title|STRING|   |
|canCancel|BOOLEAN|   |

## Examples
les can be found at [[VS:Progress Dialog]].

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYeld](ProgressDlgYeld.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
