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

```pascal
ProgressDlgYield( Len ( dynaChar ) );

BEGIN
	{Set Initial Focus Point Info}
	TmpFocusPtHandle := GetObject(gFocusPtName[gStartSceneNum, FocusPtNum]);
	IF TmpFocusPtHandle <> NIL THEN SetFocusPtValues(TmpFocusPtHandle, gStartSceneNum, FocusPtNum);
	ProgressDlgYield( 1 );
	gInitMesgString := Concat(gInitMesgString, '.');
	ProgressDlgSetMeter(gInitMesgString);
	IF Len(gInitMesgString) > 50 THEN gInitMesgString := Concat( kPIS5002, ' ');
END; {Focus Point Init}
```
```python
import vs

# Increases the progress.
count = 5

vs.ProgressDlgYield(count)
```

## See Also
[ProgressDlgOpen](ProgressDlgOpen.md) | [ProgressDlgClose](ProgressDlgClose.md) | [ProgressDlgSetTopMsg](ProgressDlgSetTopMsg.md) | [ProgressDlgSetBotMsg](ProgressDlgSetBotMsg.md) | [ProgressDlgSetMeter](ProgressDlgSetMeter.md) | [ProgressDlgStart](ProgressDlgStart.md) | [ProgressDlgEnd](ProgressDlgEnd.md) | [ProgressDlgHasCancel](ProgressDlgHasCancel.md) | [ProgressDlgYield](ProgressDlgYield.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
