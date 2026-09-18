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

```pascal
{prepare progress dialog}
kProgressDlgStr := GetPlugInString(6012);
ProgressDlgOpen( kProgressDlgStr, FALSE );
ProgressDlgStart( 100.0, GetFileSize (gImportFilePath) );

kPIS5000 := 'Initializing Lights';
kPIS5001 := 'Initializing Gobo Projectors';
kPIS5002 := 'Initializing Focus Points';
kPIS5010 := 'Initializing';}
ProgressDlgOpen(kAnnScenesStr, FALSE);
ProgressDlgSetMeter( kPIS5010 );
If ResourceIsOK Then BEGIN END;
PrefRecHand := GetObject(kSLPrefRec);
DataExchangeSuspend := FALSE;
```
```python
import vs

# Show a progress dialog that doesn't interrupt the script.
title = 'Example'
canCancel = True

vs.ProgressDlgOpen(title, canCancel)
```

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
