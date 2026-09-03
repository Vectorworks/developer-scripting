# vstGetDataString

## Description
Gets tool data.

```pascal
PROCEDURE vstGetDataString(
				inDataID    : LONGINT;
				VAR outData : DYNARRAY [] OF CHAR;
				VAR result  : BOOLEAN);
```

```python
def vs.vstGetDataString(inDataID):
    return (outData, result)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|outData|DYNARRAY [] OF CHAR|Output parameter.|
|result|BOOLEAN|Output parameter.|

## Remarks
Use a STRING rather than a DYNARRAY [] OF CHAR.  Currently DYNARRAY will cause VW to crash. (VW 2010)

## Examples
```pascal
vstGetDataString (kStringDataID_Auth, authorizer, result);
IF NOT result THEN
BEGIN
	authorizer := '???';
	vstSetDataString (kStringDataID_Auth, authorizer, result);

		BEGIN
			dataFieldID := (2*i + 1)*10 + j;
			vstGetDataString (dataFieldID, tempStr, result);
			gObjectData [i, j] := tempStr;
{
writeln (' ## i = ',i,'  j = ',j,'    dataFieldID = ',dataFieldID ,'    tempStr = ',tempStr,'    result = ',result);
}

vstGetDataString(kStrDataID_ShowName ,ShowName,result);
IF NOT result THEN
	BEGIN
	IF NOT GetSavedSetting(kFocusPtSavedSettings,kFocusPtShowName,ShowName) THEN
		ShowName := 'True';
```
```python
import vs

# Gets tool data.
inDataID = 1

outData, result = vs.vstGetDataString(inDataID)
vs.Message('vstGetDataString returned: ' + str((outData, result)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
