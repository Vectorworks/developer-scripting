# IsLSByClass

## Description
Function IsLSByClass returns whether a class line style is used for the referenced object.

```pascal
FUNCTION IsLSByClass(h : HANDLE): BOOLEAN;
```

```python
def vs.IsLSByClass(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns an indication of whether the class line style is used for the object referenced by h.
[sd 8/19/98]

## Examples
```pascal
DWidth := (Length-2*PFR-IFR)/2;
DoorThk := unitsPerInch * kDoorThk;
kickHeight := pKick_Height;
KickInset := pKick_Inset;
IsLineStyleByClass := IsLSByClass( parmHand );
QD3Ddelta := kQD3Ddelta*unitsPerInch;
LengthRightp := Length;
gTopDrawerHeight := kTopDrawerHeight*unitsPerInch;
DecodeClassName( gHiddenClass, pHidden );

GetPenFore( H, tmpStruct.NotesFormat.PenFore.red, tmpStruct.NotesFormat.PenFore.green, tmpStruct.NotesFormat.PenFore.blue );
tmpStruct.NotesFormat.lineStyle := GetLSN( H );
tmpStruct.NotesFormat.lineWeight := GetLW( H );
tmpStruct.NotesFormat.penColByClass := IsPenColorByClass( H );
tmpStruct.NotesFormat.LSByClass := IsLSByClass( H );
tmpStruct.NotesFormat.LWByClass := IsLWByClass( H );
tmpStruct.NotesFormat.FillPat := GetFPat( H );
GetFillFore( H, tmpStruct.NotesFormat.FillFore.red, tmpStruct.NotesFormat.FillFore.green, tmpStruct.NotesFormat.FillFore.blue );
GetFillBack( H, tmpStruct.NotesFormat.FillBack.red, tmpStruct.NotesFormat.FillBack.green, tmpStruct.NotesFormat.FillBack.blue );

	END;
END;
IF (ok) & (linestyleDo) & (linestyleVa <> mT) THEN BEGIN
	if not ObjectHasLS(h) then ok := false else BEGIN
		IF IsLSByClass(h)
			THEN num1 := GetClLSN(GetClass(h))
			ELSE num1 := GetLSN(h);
		num2 := Str2Num(linestyleVa);
		ok := (ok) & (((linestyleOp = '=' ) & (num1 =  num2)) |
		              ((linestyleOp = '<' ) & (num1 <  num2)) |
		              ((linestyleOp = '>' ) & (num1 >  num2)) |
```
```python
if not vs.IsLSByClass( objHand ):
	penPat	= vs.GetLSN( objHand )
	vs.PenPatN( penPat )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
