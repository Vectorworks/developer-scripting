# ProgressDlgSetMeter

## Description
Set progress meter message of a progress dialog.

```pascal
PROCEDURE ProgressDlgSetMeter(message : STRING);
```

```python
def vs.ProgressDlgSetMeter(message):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|STRING|   |

## Examples
les can be found at [[VS:Progress Dialog]].

```pascal
CurrentFrame := 0;
gInitMesgString:= Concat(kPIS5000,' ');
ProgressDlgSetMeter(gInitMesgString);
```
```python
import vs

# Set progress meter message of a progress dialog.
message = 'Hello Vectorworks'

vs.ProgressDlgSetMeter(message)
```

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
