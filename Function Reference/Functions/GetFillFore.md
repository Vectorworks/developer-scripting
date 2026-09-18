# GetFillFore

## Description
Procedure GetFillFore returns the fill foreground color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetFillFore(
				h         : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetFillFore(h):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Examples
#### VectorScript ####
```pascal
GetFillFore(handleToObject,redValue,greenValue,blueValue);
```
#### Python ####
```python
red_value, green_value, blue_value = vs.GetFillFore(vs.FSActLayer())
```

```pascal
{set Callout Fill Pattern from the FPat of the TextNote's text block}
SetFPat( CNH, GetFPat( textFoundH ) );
{set Callout Fill Pattern Fore color from the FPat fore color of the TextNote's text block}
GetFillFore( textFoundH, red, green, blue );
SetFillFore( CNH, red, green, blue );
{set Callout Fill Pattern Back color from the FPat Back color of the TextNote's text block}
GetFillBack( textFoundH, red, green, blue );
SetFillBack( CNH, red, green, blue );

IF (ok) & (fillforeDo) & (fillforeVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsFillColorByClass(h)
			THEN GetClFillFore(GetClass(h), r, g, b)
			ELSE GetFillFore(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(fillforeVa);
		ok := (ok) & (((fillforeOp = '=' ) & (num1 =  num2)) |
		              ((fillforeOp = '<' ) & (num1 <  num2)) |

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

vs.SetFillBack(objH, vs.GetFillBack(parentH))
vs.SetFillFore(objH, vs.GetFillFore(parentH))
vs.SetPenBack(objH, vs.GetPenBack(parentH))
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
vs.SetMarker(objH, start, end, style, size)
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) | [ColorIndexToRGB](ColorIndexToRGB.md) | [GetFillBack](GetFillBack.md) | [GetPenFore](GetPenFore.md) | [GetPenBack](GetPenBack.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
