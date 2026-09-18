# GetPenFore

## Description
Procedure GetPenFore returns the pen foreground color components of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetPenFore(
				h         : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetPenFore(h):
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
GetPenFore(handleToObject,redValue,greenValue,blueValue);
```
#### Python ####
```python
red_value, green_value, blue_value = vs.GetPenFore(handleToObject)
```

```pascal
BEGIN
	GetPenFore(gLine,R,G,B);
	thk := getLW(gLine);
END;

BEGIN
	GetPenFore (gWallHand,r,g,b);
	PenFore (r,g,b);
	Pensize (GetLW (gWallHand));
	PenPatN (GetLSN (gWallHand));
	GetFillBack (gWallHand,r,g,b);

if arcLineH <> NIl then SetLSN( CNH, GetLSN( arcLineH ) ) ELSE SetLSN( CNH, GetLSN( arrowLineH ) );
{set Callout Line thickness from the TextNote Group LW}
if arcLineH <> NIl then SetLW( CNH, GetLW( arcLineH ) ) ELSE SetLW( CNH, GetLW( arrowLineH ) );
{set Callout PenFore from the TextNote text block PenFore}
GetPenFore( textFoundH, red, green, blue );
SetPenFore( CNH, red, green, blue );
{set Callout PenFore from the TextNote Group PenFore
if arcLineH <> NIl then GetPenFore( arcLineH, red, green, blue ) ELSE GetPenFore( arrowLineH, red, green, blue );
SetPenFore( CNH, red, green, blue );}
```
```python
else:
	colorR, colorG, colorB = vs.GetPenFore( gObjHandle )
	vs.SetPenFore( hTmpHand, ( colorR, colorG, colorB )	)

if not vs.IsPenColorByClass( objHand ):
	rgb = vs.GetPenFore( objHand )
	vs.PenFore( rgb )

vs.SetFillBack(objH, vs.GetFillBack(parentH))
vs.SetFillFore(objH, vs.GetFillFore(parentH))
vs.SetPenBack(objH, vs.GetPenBack(parentH))
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
vs.SetMarker(objH, start, end, style, size)
vs.SetOpacity(objH, vs.GetOpacity(parentH))
```

## See Also
VS Functions: [ColorIndexToRGB](ColorIndexToRGB.md) | [RGBToColorIndex](RGBToColorIndex.md) | [GetPenBack](GetPenBack.md) | [GetFillFore](GetFillFore.md) | [GetFillBack](GetFillBack.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
