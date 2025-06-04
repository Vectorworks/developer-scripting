# ProgressDlgStart

## Description
Start a progress context. This defines progress percentage and loop count for ProgressDlgYield calls. LoopCount is fit in the Percentage of the progress

```pascal
PROCEDURE ProgressDlgStart(
				Percentage : REAL;
				LoopCount  : LONGINT);
```

```python
def vs.ProgressDlgStart(Percentage, LoopCount):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Percentage|REAL|   |
|LoopCount|LONGINT|   |

## Examples
les can be found at [[VS:Progress Dialog]].

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
