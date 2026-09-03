# Wait

## Description
Procedure Wait delays execution in VectorScript for a specified number of seconds.

When paused, a VectorScript routine stops at the point where Wait is encountered.

```pascal
PROCEDURE Wait(seconds : INTEGER);
```

```python
def vs.Wait(seconds):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|seconds|INTEGER|Number of seconds to pause script execution.|

## Examples
#### VectorScript ####
```pascal
Wait(3);
{pauses execution for 3 seconds}
```
#### Python ####
```python

```

```pascal
BEGIN
	AlertInform (GetPluginString (5024), '', TRUE);
	Wait(3);
END

BEGIN
	message (GetPluginString (5001));
	Wait(1);
	DSelectAll;
	VSave('UpdateObjectsTempView');
	DoMenuTextByName(GetLocStr(11050,32), 1);{'Standard Views'}

		NumLights := Count(R IN [kInstObjName]);
		Message(GetPlugInString(5000), CurInstNum, GetPlugInString(5001), NumLights);
		TmpCnt := Count(kInstObjName.kDeviceTypeFieldName=kSAccDevice);
		ForEachObject(ExportLightInfo, (R IN [kInstObjName]));
		Wait(1);
		ClrMessage;
		Close(ExportFile);
	END; {DidCancel file Put Dlog}
END;
```
```python
vs.Wait(seconds)
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
