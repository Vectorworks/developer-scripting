# GetLSN

## Description
Function GetLSN returns the line style of the referenced object.

```pascal
FUNCTION GetLSN(h : HANDLE): LONGINT;
```

```python
def vs.GetLSN(h):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
*\_c\_* (2016.02.29): Returns a name list index, while the older routine [GetLS](GetLS.md) returned a dash style index. 

```pascal
styleName := Index2Name(-GetLSN(FSActLayer));
{ returns the name of the dash style defintion of the first selected object }
```

## Examples
```pascal
BEGIN
	GetPenFore (gWallHand,r,g,b);
	PenFore (r,g,b);
	Pensize (GetLW (gWallHand));
	PenPatN (GetLSN (gWallHand));
	GetFillBack (gWallHand,r,g,b);
	FillBack (r,g,b);
END;

{====================== Set Attributes ======================}
{set Callout Line style from the TextNote Group LS}
if arcLineH <> NIl then SetLSN( CNH, GetLSN( arcLineH ) ) ELSE SetLSN( CNH, GetLSN( arrowLineH ) );
{set Callout Line thickness from the TextNote Group LW}
if arcLineH <> NIl then SetLW( CNH, GetLW( arcLineH ) ) ELSE SetLW( CNH, GetLW( arrowLineH ) );
{set Callout PenFore from the TextNote text block PenFore}
GetPenFore( textFoundH, red, green, blue );

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

if setLineWeight:
	vs.SetLW(objH, vs.GetLW(parentH))
vs.SetLSN(objH, vs.GetLSN(parentH))
```

## See Also
VS Functions:
[SetLSN](SetLSN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
