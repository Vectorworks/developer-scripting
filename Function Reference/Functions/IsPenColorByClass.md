# IsPenColorByClass

## Description
Function IsPenColorByClass returns whether class pen colors are used for the referenced object.

```pascal
FUNCTION IsPenColorByClass(h : HANDLE): BOOLEAN;
```

```python
def vs.IsPenColorByClass(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns an indication of whether the class pen colors are used for the object referenced by h.

[sd 8/19/98]

## Examples
```pascal
tmpStruct.NotesFormat.size		:= GetTextSize( H, noteFirstPos-1 );
GetPenFore( H, tmpStruct.NotesFormat.PenFore.red, tmpStruct.NotesFormat.PenFore.green, tmpStruct.NotesFormat.PenFore.blue );
tmpStruct.NotesFormat.lineStyle := GetLSN( H );
tmpStruct.NotesFormat.lineWeight := GetLW( H );
tmpStruct.NotesFormat.penColByClass := IsPenColorByClass( H );
tmpStruct.NotesFormat.LSByClass := IsLSByClass( H );
tmpStruct.NotesFormat.LWByClass := IsLWByClass( H );
tmpStruct.NotesFormat.FillPat := GetFPat( H );
GetFillFore( H, tmpStruct.NotesFormat.FillFore.red, tmpStruct.NotesFormat.FillFore.green, tmpStruct.NotesFormat.FillFore.blue );

	END;
END;
IF (ok) & (penbackDo) & (penbackVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsPenColorByClass(h)
			THEN GetClPenBack(GetClass(h), r, g, b)
			ELSE GetPenBack(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(penbackVa);
		ok := (ok) & (((penbackOp = '=' ) & (num1 =  num2)) |
		              ((penbackOp = '<' ) & (num1 <  num2)) |

	WhiteR := 65535;
	WhiteG := 65535;
	WhiteB := 65535;
	END;
IF IsPenColorByClass(ActiveParmHand) THEN
	BEGIN
	SetPenColorByClass(h);
	END
```
```python
if vs.IsPenColorByClass(gObjHandle):
	vs.SetPenColorByClass(hTmpHand)

if not vs.IsPenColorByClass( objHand ):
	rgb = vs.GetPenFore( objHand )
	vs.PenFore( rgb )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
