# NewField

## Description
Creates a new field in a specified record format. If the record does not exist, a new one is created using the specified record name.

Please refer to the [Script Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#record---worksheet-field-types) for specific field data types and formatting.

```pascal
PROCEDURE NewField(
				recName    : STRING;
				fieldName  : STRING;
				fieldValue : DYNARRAY[] of CHAR;
				fType      : INTEGER;
				fFlag      : INTEGER);
```

```python
def vs.NewField(recName, fieldName, fieldValue, fType, fFlag):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|recName|STRING|Name of record to which field will be added.|
|fieldName|STRING|Name of new field.|
|fieldValue|DYNARRAY[] of CHAR|Default value for new field.|
|fType|INTEGER|Data type of new field.|
|fFlag|INTEGER|Display style of field.|

## Remarks
If the fieldName argument is longer than 20 characters, it will be truncated to 20 characters, without warning. The recName argument can be up to something like 60 characters (I think).

## Examples
#### VectorScript ####
```pascal
NewField('Part Info','Serial No.','A-0000',4,0);
```
#### Python ####
```python

```

```pascal
	{Store the body notes in the GN's Profile Group and in the temp... arrays as well}
	BeginGroup;
{check if the hidRecord exists in the document and create it if not}
		IF ( GetObject(kHidRecName) = NIL ) THEN BEGIN
			NewField(kHidRecName, kDatabaseName, '', 4, 0);
			NewField(kHidRecName, kDatabaseUUID, '', 4, 0);
			NewField(kHidRecName, kNoteDescrip,  '', 4, 0);
			NewField(kHidRecName, kNoteUUID,     '', 4, 0);
			NewField(kHidRecName, kText,         '', 4, 0);

BEGIN
NewField(kHiddenRecName,'Marker','',4,0);
NewField(kHiddenRecName,'WhichOne','',4,0);
SetObjectVariableBoolean(GetObject(kHiddenRecName),900,FALSE);
END;

BEGIN
	NewField(kTempFmtName, kRecChoiceName, kEmpty, 4, 0);
	NewField(kTempFmtName, kSymChoiceName, kEmpty, 4, 0);
	NewField(kTempFmtName, kDupModeName, kTrueStr, 2, 1);
	NewField(kTempFmtName, kPrevIDName, kEmpty, 4, 0);
	SetObjectVariableBoolean(GetObject(kTempFmtName),900,FALSE);
```
```python
if vs.GetObject( kHiddenRecName ) == None:
	vs.NewField( kHiddenRecName, 'IEMName', '', 4 ,0 )
	vs.NewField( kHiddenRecName, 'IEMAction', '', 4, 0 )
	vs.SetObjectVariableBoolean( vs.GetObject( kHiddenRecName ), 900, False )
```
See also in tutorials: [08. Attach and Read Records on Objects](ai%20examples/08_AttachAndReadRecords.md), [24. Auto-Populating Database Row](ai%20examples/24_WorksheetDBRowAutoPopulate.md), [26. Sorting and Grouping with `SetWSColumnOperators`](ai%20examples/26_WorksheetSortAndGroup.md)

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
