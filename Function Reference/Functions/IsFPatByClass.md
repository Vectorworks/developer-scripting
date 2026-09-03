# IsFPatByClass

## Description
Function IsFPatByClass whether a class fill pattern is used for the referenced object.

```pascal
FUNCTION IsFPatByClass(h : HANDLE): BOOLEAN;
```

```python
def vs.IsFPatByClass(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns an indication of whether the class fill pattern is used for the object referenced by h.
[sd  8/19/98]

## Examples
```pascal
BEGIN
	IF NOT IsFPatByClass(parentHand) THEN
	BEGIN
		patID := GetFPat(parentHand);
		IF patID < 0 THEN
		BEGIN
			resHand	:= GetObject(Index2Name(-patID));
			resType	:= GetTypeN(resHand);

	tmpStruct.NotesFormat.FillPat := GetFPat( H );
	GetFillFore( H, tmpStruct.NotesFormat.FillFore.red, tmpStruct.NotesFormat.FillFore.green, tmpStruct.NotesFormat.FillFore.blue );
	GetFillBack( H, tmpStruct.NotesFormat.FillBack.red, tmpStruct.NotesFormat.FillBack.green, tmpStruct.NotesFormat.FillBack.blue );
	tmpStruct.NotesFormat.fColByClass := IsFillColorByClass( H );
	tmpStruct.NotesFormat.FPatByClass := IsFPatByClass( H );
	tmpStruct.objClass := GetClass( H );
	Layer( GetLName( actLH  ) );
END;

	FillFore(red, green, blue);
	GetFillBack(objHand, red, green, blue);
	FillBack(red, green, blue);
END;
if not IsFPatByClass(objHand) then BEGIN
	FillPat(GetFPat(objHand));
END;
```
```python
if nFillPat != 0:
	if vs.IsFPatByClass(gObjHandle):
		vs.SetFPatByClass(hObjectHand)
	else:
		nFillPat = vs.GetFPat( gObjHandle )
		vs.SetFPat( hObjectHand, nFillPat )

if not vs.IsFPatByClass( objHand ):
	penPat	= vs.GetFPat( objHand )
	vs.FillPat( penPat )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
