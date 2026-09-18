# vstSetDataLong

## Description
VSTs store persistent data between calls using vstSetDataLong and vstGetDataLong.

```pascal
PROCEDURE vstSetDataLong(
				inDataID   : LONGINT;
				inDataVal  : LONGINT;
				VAR result : BOOLEAN);
```

```python
def vs.vstSetDataLong(inDataID, inDataVal):
    return result
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|inDataVal|LONGINT|   |
|result|BOOLEAN|Output parameter.|

## Examples
```pascal
BEGIN
	modeValue_1 := 2;
	vstSetDataLong (kModeDataID_1, modeValue_1, result);
END;

	IF GetSavedSetting('RevisionCloud','Mode1',TmpStr) THEN
		modeValue_1 := Str2Num(TmpStr)
	ELSE
		modeValue_1 := 1;
	vstSetDataLong (kModeDataID_1, modeValue_1, result);
END;

BEGIN
	modeValue := 2;
	vstSetDataLong( kModeDataID, modeValue, result );
END;
```
```python
import vs

# VSTs store persistent data between calls using vstSetDataLong and
# vstGetDataLong.
inDataID = 1
inDataVal = 2

result = vs.vstSetDataLong(inDataID, inDataVal)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
