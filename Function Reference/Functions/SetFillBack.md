# SetFillBack

## Description
Procedure SetFillBack sets the fill background color setting of the specified object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetFillBack(
				h     : HANDLE;
				color : LONGINT);
```

```python
def vs.SetFillBack(h, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|color|LONGINT|RGB color value.|

## Remarks
\_c\_: This Procedure will also accept a single INTEGER Color Palette Index value in lieu of three LONGINT RGB values for the COLOR parameter. The Color index can be obtained with [RGBToColorIndex](RGBToColorIndex.md). See remarks under [SetPenFore](SetPenFore.md) for more infos. On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].
; Warning: SetFillBack, SetFillFore will remove the "ByClass" attribute of the PEN as well. Remember to parse for it and restore it.

## Examples
#### VectorScript ####
```pascal
{ Sets the Fill Background to black }
SetFillBack(h, 0, 0, 0); { using rgb values }
SetFillBack(h, 255); { using color index, be careful with color indexes after VW12 }
{ Conversely, GetFillBack will only return RGB values. }
```
#### Python ####
```python
vs.SetFillBack( h, (0, 0, 0) ) # using rgb values in a tuple
vs.SetFillBack( h, (65535, 0, 0) ) # red color - note that the values are 32-bit
vs.SetFillBack( h, (0xFFFF, 0, 0) ) # red color - or you can use hex numbers in python
vs.SetFillBack( h, 255 ) # using color index, be careful with color indexes after VW12
```

```pascal
BEGIN
	FFillFore (R, G, B);
	SetFillFore (objectH, R, G, B);
	FFillBack (R, G, B);
	SetFillBack (objectH, R, G, B);
END;

	SetTextJust(LNewObj,2);
	SetTextVerticalAlign(LNewObj,3);
	setfpat(lnewobj,GetFPat(parmHand));
	GetFillBack(parmHand,red,grn,bl);
	SetFillBack(LNewObj,red,grn,bl);
	popattrs;
END;

BEGIN
	SetFillFore( childH, redValue,		greenValue,		blueValue );
	SetFillBack( childH, redValueBack,	greenValueBack, blueValueBack );
END;
```
```python
if vs.GetPref( 16 ):
	vs.SetFillBack( vs.LNewObj(), ( 65535, 65535, 65535 ) )
else:
	vs.SetFillBack( vs.LNewObj(), ( 0, 0, 0 ) )

vs.SetFillBack(objH, vs.GetFillBack(parentH))
vs.SetFillFore(objH, vs.GetFillFore(parentH))
vs.SetPenBack(objH, vs.GetPenBack(parentH))
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
