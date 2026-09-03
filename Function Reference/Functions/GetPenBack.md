# GetPenBack

## Description
Procedure GetPenBack returns the pen (pattern) background color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetPenBack(
				h         : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetPenBack(h):
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
PROCEDURE Example;
VAR
h :HANDLE;
r, g, b :LONGINT;
BEGIN
h := FSActLayer;
GetPenBack(h, r, g, b);
Message('r= ', r, ' g= ', g, ' b= ', b);
END;
RUN(Example);
```
#### Python ####
```python
def example():
	h = vs.FSActLayer()
	r, g, b = vs.GetPenBack(h)
	vs.Message('r= ', r, ' g= ', g, ' b= ', b)

example()
```

```pascal
{set Callout PenFore from the TextNote Group PenFore
if arcLineH <> NIl then GetPenFore( arcLineH, red, green, blue ) ELSE GetPenFore( arrowLineH, red, green, blue );
SetPenFore( CNH, red, green, blue );}
{set Callout PenBack from the TextNote Group PenBack}
if arcLineH <> NIl then GetPenBack( arcLineH, red, green, blue ) ELSE GetPenBack( arrowLineH, red, green, blue );
SetPenBack( CNH, red, green, blue );

IF (ok) & (penbackDo) & (penbackVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsPenColorByClass(h)
			THEN GetClPenBack(GetClass(h), r, g, b)
			ELSE GetPenBack(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(penbackVa);
		ok := (ok) & (((penbackOp = '=' ) & (num1 =  num2)) |
		              ((penbackOp = '<' ) & (num1 <  num2)) |

BEGIN
GetPenBack(ActiveParmHand,colorR, colorG, colorB);
SetPenBack(h,colorR, colorG, colorB);
GetPenFore(ActiveParmHand,colorR, colorG, colorB);
SetPenFore(h,colorR, colorG, colorB);
END;
```
```python
colorR, colorG, colorB = vs.GetPenBack( gObjHandle )
vs.SetPenBack( hTmpHand, ( colorR, colorG, colorB ) )

rgb = vs.GetPenBack( objHand )
vs.PenBack( rgb )

vs.SetFillBack(objH, vs.GetFillBack(parentH))
vs.SetFillFore(objH, vs.GetFillFore(parentH))
vs.SetPenBack(objH, vs.GetPenBack(parentH))
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
vs.SetMarker(objH, start, end, style, size)
vs.SetOpacity(objH, vs.GetOpacity(parentH))
```

## See Also
VS Functions: [RGBToColorIndex](RGBToColorIndex.md) | [ColorIndexToRGB](ColorIndexToRGB.md) | [GetFillFore](GetFillFore.md) | [GetFillBack](GetFillBack.md) | [GetPenFore](GetPenFore.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
