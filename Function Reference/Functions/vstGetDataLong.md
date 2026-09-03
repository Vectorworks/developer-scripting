# vstGetDataLong

## Description
VSTs store persistent data between calls using vstSetDataLong and vstGetDataLong.

```pascal
PROCEDURE vstGetDataLong(
				inDataID    : LONGINT;
				VAR outData : LONGINT;
				VAR result  : BOOLEAN);
```

```python
def vs.vstGetDataLong(inDataID):
    return (outData, result)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|outData|LONGINT|Output parameter.|
|result|BOOLEAN|Output parameter.|

## Examples
```pascal
vstGetDataLong (kModeDataID_1, modeValue_1, result);
IF NOT result THEN
BEGIN
	modeValue_1 := 2;
	vstSetDataLong (kModeDataID_1, modeValue_1, result);

vstGetDataLong (kModeDataID_1, modeValue_1, result);
IF NOT result THEN
BEGIN
	IF GetSavedSetting('RevisionCloud','Mode1',TmpStr) THEN
		modeValue_1 := Str2Num(TmpStr)

BEGIN
	VSTSetPtBehavior( kTwoPointTool );
	vstGetDataLong( kModeDataID, modeValue, result );
	IF NOT result THEN
	BEGIN
		modeValue := 2;
		vstSetDataLong( kModeDataID, modeValue, result );
```
```python
import vs

# VSTs store persistent data between calls using vstSetDataLong and
# vstGetDataLong.
inDataID = 1

outData, result = vs.vstGetDataLong(inDataID)
vs.Message('vstGetDataLong returned: ' + str((outData, result)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
