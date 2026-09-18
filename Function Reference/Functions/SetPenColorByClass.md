# SetPenColorByClass

## Description
Procedure SetPenColorByClass sets the referenced object to use the class attribute pen colors.

```pascal
PROCEDURE SetPenColorByClass(h : HANDLE);
```

```python
def vs.SetPenColorByClass(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Sets so that the class pen colors are used for the object referenced by h.

## Examples
```pascal
IF attrNum [7] THEN SetPenColorByClass (objectH)
ELSE IF option = 2 THEN
BEGIN
	FPenFore (R, G, B);
	SetPenFore (objectH, R, G, B);
END;

IF tmpStruct.NotesFormat.penColByClass THEN SetPenColorByClass( gnH )
	ELSE SetPenFore( gnH, tmpStruct.NotesFormat.PenFore.red, tmpStruct.NotesFormat.PenFore.green, tmpStruct.NotesFormat.PenFore.blue );
IF tmpStruct.NotesFormat.LSByClass THEN SetLSByClass( gnH )
	ELSE SetLSN( gnH, tmpStruct.NotesFormat.lineStyle );
IF tmpStruct.NotesFormat.LWByClass THEN SetLWByClass( gnH )
	ELSE SetLW( gnH, tmpStruct.NotesFormat.lineWeight );

BEGIN
SetPenColorByClass(h);
END
```
```python
if vs.IsPenColorByClass(gObjHandle):
	vs.SetPenColorByClass(hTmpHand)

if setLineWeight:
	vs.SetLWByClass( objH )
vs.SetMarkerByClass( objH )
vs.SetPenColorByClass( objH )
vs.SetOpacityByClass( objH )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
