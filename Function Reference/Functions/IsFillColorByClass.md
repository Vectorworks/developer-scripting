# IsFillColorByClass

## Description
Function IsFillColorByClass returns whether class fill colors are used for the referenced object.

```pascal
FUNCTION IsFillColorByClass(h : HANDLE): BOOLEAN;
```

```python
def vs.IsFillColorByClass(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns an indication of whether the class fill colors are used for the object referenced by h.
[sd 8/19/98]

## Examples
```pascal
	tmpStruct.NotesFormat.LWByClass := IsLWByClass( H );
	tmpStruct.NotesFormat.FillPat := GetFPat( H );
	GetFillFore( H, tmpStruct.NotesFormat.FillFore.red, tmpStruct.NotesFormat.FillFore.green, tmpStruct.NotesFormat.FillFore.blue );
	GetFillBack( H, tmpStruct.NotesFormat.FillBack.red, tmpStruct.NotesFormat.FillBack.green, tmpStruct.NotesFormat.FillBack.blue );
	tmpStruct.NotesFormat.fColByClass := IsFillColorByClass( H );
	tmpStruct.NotesFormat.FPatByClass := IsFPatByClass( H );
	tmpStruct.objClass := GetClass( H );
	Layer( GetLName( actLH  ) );
END;

	END;
END;
IF (ok) & (fillbackDo) & (fillbackVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsFillColorByClass(h)
			THEN GetClFillBack(GetClass(h), r, g, b)
			ELSE GetFillBack(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(fillbackVa);
		ok := (ok) & (((fillbackOp = '=' ) & (num1 =  num2)) |
		              ((fillbackOp = '<' ) & (num1 <  num2)) |

if not IsFillColorByClass(objHand) then BEGIN
	GetFillFore(objHand, red, green, blue);
	FillFore(red, green, blue);
	GetFillBack(objHand, red, green, blue);
	FillBack(red, green, blue);
END;
```
```python
if vs.IsFillColorByClass(gObjHandle):
	vs.SetFillColorByClass(hTmpHand)
else:
	colorR, colorG, colorB = vs.GetFillFore( gObjHandle )
	vs.SetFillFore( hTmpHand, ( colorR, colorG, colorB ) )

if not vs.IsFillColorByClass( objHand ):
	rgb = vs.GetFillFore( objHand )
	vs.FillFore( rgb )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
