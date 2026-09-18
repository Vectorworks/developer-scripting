# IsLWByClass

## Description
Function IsLWByClass returns whether a class line weight is used for the referenced object.

```pascal
FUNCTION IsLWByClass(h : HANDLE): BOOLEAN;
```

```python
def vs.IsLWByClass(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns an indication of whether the class line weight is used for the object referenced by h.
[sd 8/19/98]

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
symDefHandle, h :HANDLE;

PROCEDURE AlertMe;
BEGIN
Message(GetSDName(symDefHandle));
SetSelect(h);
END;

BEGIN
DSelectAll;
ClrMessage;
symDefHandle := FSymDef;
WHILE symDefHandle <> NIL DO BEGIN
h := FInSymDef(symDefHandle);
WHILE h <> NIL DO BEGIN
IF IsLWByClass(h) THEN AlertMe;
h := NextObj(h);
END;
symDefHandle := NextObj(symDefHandle);
END;
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
tmpStruct.NotesFormat.lineStyle := GetLSN( H );
tmpStruct.NotesFormat.lineWeight := GetLW( H );
tmpStruct.NotesFormat.penColByClass := IsPenColorByClass( H );
tmpStruct.NotesFormat.LSByClass := IsLSByClass( H );
tmpStruct.NotesFormat.LWByClass := IsLWByClass( H );
tmpStruct.NotesFormat.FillPat := GetFPat( H );
GetFillFore( H, tmpStruct.NotesFormat.FillFore.red, tmpStruct.NotesFormat.FillFore.green, tmpStruct.NotesFormat.FillFore.blue );
GetFillBack( H, tmpStruct.NotesFormat.FillBack.red, tmpStruct.NotesFormat.FillBack.green, tmpStruct.NotesFormat.FillBack.blue );
tmpStruct.NotesFormat.fColByClass := IsFillColorByClass( H );

IF IsLWByClass(ActiveParmHand) THEN
	SetLWByClass(DupPath)
ELSE
	BEGIN
	lw := GetLW(ActiveParmHand);
	SetLW(DupPath, lw);
	END;

END;
if not IsLSByClass(objHand) then BEGIN
	PenPatN(GetLSN(objHand));
END;
if not IsLWByClass(objHand) then BEGIN
	PenSize(GetLW(objHand));
END;
```
```python
if vs.IsLWByClass(gObjHandle):
	vs.SetLWByClass(hObjectHand)
else:
	nLineWeight = vs.GetLW ( gObjHandle )
	vs.SetLW( hObjectHand, nLineWeight )

if not vs.IsLWByClass( objHand ):
	penSize	= vs.GetLW( objHand )
	vs.PenSize( penSize )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
