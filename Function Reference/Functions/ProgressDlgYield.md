# ProgressDlgYield

## Description
Increases the progress. This must be called between ProgressDlgStart and ProgressDlgEnd and defines the LoopCount index.


Note: This function was renamed from ProgressDlgYield in Vectorworks 2016

```pascal
PROCEDURE ProgressDlgYield(count : LONGINT);
```

```python
def vs.ProgressDlgYield(count):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|count|LONGINT|   |

## Examples
les can be found at [[VS:Progress Dialog]].

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
