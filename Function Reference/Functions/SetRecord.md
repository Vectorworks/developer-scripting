# SetRecord

## Description
Assigns an instance of an existing record format to the referenced object .

```pascal
PROCEDURE SetRecord(
				h      : HANDLE;
				record : STRING);
```

```python
def vs.SetRecord(h, record):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|record|STRING|Name of record to assign to object.|

## Examples
#### VectorScript ####
```pascal
SetRecord(HandleToObject,'Part Info');
```
#### Python ####
```python

```

```pascal
BEGIN
	gNumSymbols := gNumSymbols + 1;
	SetRecord (symDefH, gRecordName);
END;

END;
for cnt1 := 1 to tmpStruct.bodyNotesCnt do BEGIN
	Locus(0, 0);
	loch := LNewObj;
	SetRecord(loch, kHidRecName);
	dynChar := '';
	for cnt2 := 1 to m_GNbodyNotesLens[ cnt1 ] DO
		dynChar := Concat(dynChar, m_GNbodyNotes[ cnt2, cnt1 ] );

BEGIN
BeginGroup;
Locus(0,0);
SetRecord(LNewObj,kHiddenRecName);
SetRField(LNewObj,kHiddenRecName,'WhichOne','DeleteMe');
EndGroup;
GroupHand:= LNewObj;
SetClass(GroupHand,noneClass);
```
```python
if vs.GetObject( strMarkerActualName ) != None:
	vs.BeginGroup()
	vs.Locus(0,0)
	vs.SetRecord( vs.LNewObj(), kHiddenRecName )
	vs.SetRField( vs.LNewObj(), kHiddenRecName, 'IEMAction', 'DeleteMe' )
	vs.EndGroup()
	hGroupHand = vs.LNewObj()
```
See also in tutorials: [08. Attach and Read Records on Objects](ai%20examples/08_AttachAndReadRecords.md), [24. Auto-Populating Database Row](ai%20examples/24_WorksheetDBRowAutoPopulate.md), [26. Sorting and Grouping with `SetWSColumnOperators`](ai%20examples/26_WorksheetSortAndGroup.md)

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
