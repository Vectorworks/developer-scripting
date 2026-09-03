# SetLWByClass

## Description
Procedure SetLWByClass sets the referenced object to use the class attribute line weight.

```pascal
PROCEDURE SetLWByClass(h : HANDLE);
```

```python
def vs.SetLWByClass(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Sets so that the class line weight is used for the object referenced by h.

## Examples
```pascal
IF attrNum [5] THEN SetLWByClass (objectH)
ELSE IF option = 2 THEN SetLW (objectH, FPenSize);

IF tmpStruct.NotesFormat.penColByClass THEN SetPenColorByClass( gnH )
	ELSE SetPenFore( gnH, tmpStruct.NotesFormat.PenFore.red, tmpStruct.NotesFormat.PenFore.green, tmpStruct.NotesFormat.PenFore.blue );
IF tmpStruct.NotesFormat.LSByClass THEN SetLSByClass( gnH )
	ELSE SetLSN( gnH, tmpStruct.NotesFormat.lineStyle );
IF tmpStruct.NotesFormat.LWByClass THEN SetLWByClass( gnH )
	ELSE SetLW( gnH, tmpStruct.NotesFormat.lineWeight );

IF IsLWByClass(ActiveParmHand) THEN
	SetLWByClass(DupPath)
ELSE
	BEGIN
	lw := GetLW(ActiveParmHand);
	SetLW(DupPath, lw);
	END;
```
```python
if vs.IsLWByClass(gObjHandle):
	vs.SetLWByClass(hObjectHand)
else:
	nLineWeight = vs.GetLW ( gObjHandle )
	vs.SetLW( hObjectHand, nLineWeight )

if setLineWeight:
	vs.SetLWByClass( objH )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
