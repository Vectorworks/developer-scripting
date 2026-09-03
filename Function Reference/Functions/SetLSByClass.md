# SetLSByClass

## Description
Procedure SetLSByClass sets the referenced object to use the class attribute line style.

```pascal
PROCEDURE SetLSByClass(h : HANDLE);
```

```python
def vs.SetLSByClass(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Sets so that the class line style is used for the object referenced by h.
[sd 8/19/98]

## Examples
```pascal
	SetLW(LNewObj,kThinLine);
IF IsLineStyleByClass THEN SetLSByClass( LNewObj );
HMoveBackward(LNewObj, TRUE);
MoveTo(X,Y);
LineTo(X,Y+Length);
	IF IsLineStyleByClass THEN SetLSByClass( LNewObj );

IF attrNum [4] THEN SetLSByClass (objectH)
ELSE IF option = 2 THEN SetLSN (objectH, FPenPatN);

IF tmpStruct.NotesFormat.penColByClass THEN SetPenColorByClass( gnH )
	ELSE SetPenFore( gnH, tmpStruct.NotesFormat.PenFore.red, tmpStruct.NotesFormat.PenFore.green, tmpStruct.NotesFormat.PenFore.blue );
IF tmpStruct.NotesFormat.LSByClass THEN SetLSByClass( gnH )
	ELSE SetLSN( gnH, tmpStruct.NotesFormat.lineStyle );
IF tmpStruct.NotesFormat.LWByClass THEN SetLWByClass( gnH )
	ELSE SetLW( gnH, tmpStruct.NotesFormat.lineWeight );
```
```python
def SetAttrsByClass( objH, setLineWeight = True ):
	vs.SetFillColorByClass( objH )
	vs.SetFPatByClass( objH )
	vs.SetLSByClass( objH )
	if setLineWeight:
		vs.SetLWByClass( objH )
	vs.SetMarkerByClass( objH )
	vs.SetPenColorByClass( objH )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
