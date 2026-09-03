# vstSetDataString

## Description
Sets tool data.

```pascal
PROCEDURE vstSetDataString(
				inDataID   : LONGINT;
				inDataVal  : DYNARRAY [] OF CHAR;
				VAR result : BOOLEAN);
```

```python
def vs.vstSetDataString(inDataID, inDataVal):
    return result
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|inDataVal|DYNARRAY [] OF CHAR|   |
|result|BOOLEAN|Output parameter.|

## Remarks
Use a STRING rather than a DYNARRAY [] OF CHAR.  Currently DYNARRAY will cause VW to crash. (VW 2010)

## Examples
```pascal
BEGIN
	authorizer := '???';
	vstSetDataString (kStringDataID_Auth, authorizer, result);
END;

BEGIN
	tempStr := dataString [i, j];
	vstSetDataString (dataFieldID, tempStr, result);
END;

BEGIN
IF NOT GetSavedSetting(kFocusPtSavedSettings,kFocusPtShowName,ShowName) THEN
	ShowName := 'True';
vstSetDataString(kStrDataID_ShowName,ShowName,result);
END;
```
```python
import vs

# Sets tool data.
inDataID = 1
inDataVal = 'Example'

result = vs.vstSetDataString(inDataID, inDataVal)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
