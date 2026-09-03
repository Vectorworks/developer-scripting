# GetFldName

## Description
Returns the name of the specified field in the referenced record.

```pascal
FUNCTION GetFldName(
				h     : HANDLE;
				index : INTEGER): STRING;
```

```python
def vs.GetFldName(h, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to record.|
|index|INTEGER|Number of field whose name will be returned (in a range of 1-n).|

## Examples
#### VectorScript ####
```pascal
FName:=GetFldName(HandleToRecord,1);
```
#### Python ####
```python
FName = vs.GetFldName(HandleToRecord,1)
```

```pascal
FOR i := 1 TO nFields DO
	fieldN [i] := GetFldName (recordH, i);

FOR i := 1 TO gNFields DO
	fieldN [i] := GetFldName (recordH, i);

BEGIN
	paramName := GetFldName( recHand, parmIdx );
	IF paramName = 'OA Height' THEN
	BEGIN
		result := GetObjStoryBound( gPluginH, kTopBoundArchitID, boundType, boundStory, layerLevelType, tempOffset );
		SetObjectStoryBound( gPluginH, kTopBoundArchitID, boundType, boundStory, layerLevelType, tempOffset + ( pOA_Height - ( str2num( oldValue ) * GetPrefReal(152) / 25.4 ) ) );
```
```python
fldName = vs.GetFldName( vs.GetObject( recordName ), 1 )
fldValue = vs.GetRField( hObjectHand, recordName, fldName )
```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
