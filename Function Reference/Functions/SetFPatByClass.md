# SetFPatByClass

## Description
Procedure SetFPatByClass sets the referenced object to use the class attribute fill pattern.

```pascal
PROCEDURE SetFPatByClass(h : HANDLE);
```

```python
def vs.SetFPatByClass(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Sets so that the class fill pattern is used for the object referenced by h.
[sd 8/19/98]

## Examples
```pascal
IF attrNum [3] THEN SetFPatByClass (objectH)
ELSE IF option = 2 THEN SetFPat (objectH, FFillPat);

IF tmpStruct.NotesFormat.FPatByClass THEN SetFPatByClass( gnH )
	ELSE SetFPat( gnH, tmpStruct.NotesFormat.FillPat );
IF tmpStruct.NotesFormat.fColByClass THEN SetFillColorByClass( gnH )
	else BEGIN
		SetFillFore( gnH, tmpStruct.NotesFormat.FillFore.red, tmpStruct.NotesFormat.FillFore.green, tmpStruct.NotesFormat.FillFore.blue );
		SetFillBack( gnH, tmpStruct.NotesFormat.FillBack.red, tmpStruct.NotesFormat.FillBack.green, tmpStruct.NotesFormat.FillBack.blue );

BEGIN
{SetFPat(LNewObj,shadowFillStyle);}
SetClass(LNewObj, shadowFillName );
SetFPatByClass ( LNewObj );
SetFillColorByClass( LNewObj );
SetLW(LNewObj, 0);{ no pen drawn }
{SetPenColorByClass( LNewObj );}
END;
```
```python
if vs.IsFPatByClass(gObjHandle):
	vs.SetFPatByClass(hObjectHand)

def SetAttrsByClass( objH, setLineWeight = True ):
	vs.SetFillColorByClass( objH )
	vs.SetFPatByClass( objH )
	vs.SetLSByClass( objH )
	if setLineWeight:
		vs.SetLWByClass( objH )
	vs.SetMarkerByClass( objH )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
