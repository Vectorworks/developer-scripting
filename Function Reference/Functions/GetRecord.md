# GetRecord

## Description
Returns the handle to a specified record attached the referenced object.

```pascal
FUNCTION GetRecord(
				h   : HANDLE;
				cnt : INTEGER): HANDLE;
```

```python
def vs.GetRecord(h, cnt):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|cnt|INTEGER|Index of attached record (in a range of 1 -  n).|

## Remarks
*\_c\_*, 2015.02.24:
Please note that since the introduction of ifc data, the usual praxis of fetching plug-in records using GetRecord(h, NumRecords(h)) can bring you perhaps unexpectedly the ifc record. Use [GetParametricRecord](GetParametricRecord.md) instead, introduced from VW 2011.

## Examples
#### VectorScript ####
```pascal
handleToRecord := GetRecord(handleToObject,3);
```
#### Python ####
```python
handleToRecord = vs.GetRecord(handleToObject,3)
```

```pascal
BEGIN
	recordH := GetRecord (NIL, i);
	IF NOT IsPluginFormat (recordH) AND NOT GetObjectVariableBoolean(recordH, 700) THEN  {700 is whether or not the object is locked}
	BEGIN
		j := j + 1;
		ALLOCATE gRecordN [1..j];

BEGIN
IF (GetType(objHand) = 86) & (GetName(GetRecord(objHand,NumRecords(objHand)))= parmName) THEN {Added to make sure we don't try to set anything other than 'this' object since we need to go deep}
	BEGIN
	SetRField(objHand, parmName,FieldName, SymName);
	ResetObject(objHand);
	END;

BEGIN
	recordH := GetRecord (NIL, i);
	IF (NOT IsPluginFormat (recordH)) AND (NOT IsLocked(recordH)) THEN
	BEGIN
		recName := Copy( GetName( recordH ), 1, 5 );
		if  recName <> '__NNA'  THEN
```
```python
if (parentParametric != None) and (vs.GetTypeN(parentParametric) == kPlugInObject):
	parentRecord = vs.GetRecord(parentParametric, 1)
	if (parentRecord != None) and (vs.GetTypeN(parentRecord) == kRecordNode):
		strParentName = vs.GetName(parentRecord)
```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
