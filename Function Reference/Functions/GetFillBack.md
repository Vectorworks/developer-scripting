# GetFillBack

## Description
Procedure GetFillBack returns the fill background color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetFillBack(
				h         : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetFillBack(h):
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
GetFillBack(handleToObject,redValue,greenValue,blueValue);
```
#### Python ####
```python
red_value, green_value, blue_value = vs.GetFillBack(vs.FSActLayer())
```

```pascal
	CreateText(anno);
	SetTextJust(LNewObj,2);
	SetTextVerticalAlign(LNewObj,3);
	setfpat(lnewobj,GetFPat(parmHand));
	GetFillBack(parmHand,red,grn,bl);
	SetFillBack(LNewObj,red,grn,bl);
	popattrs;
END;

	GetPenFore (gWallHand,r,g,b);
	PenFore (r,g,b);
	Pensize (GetLW (gWallHand));
	PenPatN (GetLSN (gWallHand));
	GetFillBack (gWallHand,r,g,b);
	FillBack (r,g,b);
END;

{set Callout Fill Pattern Fore color from the FPat fore color of the TextNote's text block}
GetFillFore( textFoundH, red, green, blue );
SetFillFore( CNH, red, green, blue );
{set Callout Fill Pattern Back color from the FPat Back color of the TextNote's text block}
GetFillBack( textFoundH, red, green, blue );
SetFillBack( CNH, red, green, blue );
{====================== Set Attributes ======================}
```
```python
colorR, colorG, colorB = vs.GetFillBack( gObjHandle )
vs.SetFillBack( hTmpHand, ( colorR, colorG, colorB ) )

rgb = vs.GetFillBack( objHand )
vs.FillBack( rgb )

vs.SetFillBack(objH, vs.GetFillBack(parentH))
vs.SetFillFore(objH, vs.GetFillFore(parentH))
vs.SetPenBack(objH, vs.GetPenBack(parentH))
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
```

## See Also
VS Functions: [RGBToColorIndex](RGBToColorIndex.md) | [ColorIndexToRGB](ColorIndexToRGB.md) | [GetFillFore](GetFillFore.md) | [GetPenFore](GetPenFore.md) | [GetPenBack](GetPenBack.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
