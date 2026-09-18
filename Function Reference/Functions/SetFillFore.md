# SetFillFore

## Description
Procedure SetFillFore sets the fill foreground color setting of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetFillFore(
				h     : HANDLE;
				color : LONGINT);
```

```python
def vs.SetFillFore(h, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|color|LONGINT|RGB color value.|

## Remarks
\_c\_ 2015.05.19: This Procedure will also accept a single INTEGER Color Palette Index value in lieu of three LONGINT RGB values for the COLOR parameter. The Color index can be obtained with [RGBToColorIndex](RGBToColorIndex.md). See remarks under [SetPenFore](SetPenFore.md) for more infos. On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].

; Warning: SetFillBack, SetFillFore will remove the "ByClass" attribute of the PEN as well. Remember to parse for it and restore it.

## Examples
#### VectorScript ####
```pascal
SetFillFore(h, 65535, 0, 39321); { using RGB values }

colorIndex := RGBToColorIndex(65535, 0, 39321);
SetFillFore(h, colorIndex); { using Color Index values }
```
#### Python ####
```python
vs.SetFillFore(h, (65535, 0, 39321)) # using RGB values

colorIndex = vs.RGBToColorIndex(65535, 0, 39321)
vs.SetFillFore(h, colorIndex) # using Color Index values
```

```pascal
BEGIN
	FFillFore (R, G, B);
	SetFillFore (objectH, R, G, B);
	FFillBack (R, G, B);
	SetFillBack (objectH, R, G, B);
END;

BEGIN
	SetFillFore( childH, redValue,		greenValue,		blueValue );
	SetFillBack( childH, redValueBack,	greenValueBack, blueValueBack );
END;

{set Callout Fill Pattern from the FPat of the TextNote's text block}
SetFPat( CNH, GetFPat( textFoundH ) );
{set Callout Fill Pattern Fore color from the FPat fore color of the TextNote's text block}
GetFillFore( textFoundH, red, green, blue );
SetFillFore( CNH, red, green, blue );
{set Callout Fill Pattern Back color from the FPat Back color of the TextNote's text block}
GetFillBack( textFoundH, red, green, blue );
SetFillBack( CNH, red, green, blue );
{====================== Set Attributes ======================}
```
```python
	vs.SetFillColorByClass(hTmpHand)
else:
	colorR, colorG, colorB = vs.GetFillFore( gObjHandle )
	vs.SetFillFore( hTmpHand, ( colorR, colorG, colorB ) )

vs.SetFillBack(objH, vs.GetFillBack(parentH))
vs.SetFillFore(objH, vs.GetFillFore(parentH))
vs.SetPenBack(objH, vs.GetPenBack(parentH))
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
vs.SetMarker(objH, start, end, style, size)
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
