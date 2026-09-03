# SetPenBack

## Description
Procedure SetPenBack sets the pen background color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetPenBack(
				h     : HANDLE;
				color : LONGINT);
```

```python
def vs.SetPenBack(h, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|color|LONGINT|RGB color value.|

## Remarks
(\_c\_ 2015.05.18): This Vectorscript routine responds to multiple types of notations:

Vectorscript:
* Singular [ color index](RGBToColorIndex.md):
*: <code>colorIndex := RGBToColorIndex(65535, 0, 0);</code>
*: <code>SetPenBack(FSActLayer, colorIndex);</code>
* Three RGB longints:
*: <code>SetPenBack(FSActLayer, 65535, 0, 0);</code>
 
Python:
* Singular color index:
*: <code>vs.SetPenBack(vs.FSActLayer(), vs.RGBToColorIndex(65535, 0, 0)) </code>
* Three longints in a tuple:
*: <code>vs.SetPenBack(vs.FSActLayer(), (65535, 0, 0)) </code>
* Three hex numbers in a tuple:
*: <code>vs.SetPenBack(vs.FSActLayer(), (0xFFFF, 0, 0)) </code>

On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].
; Warning: SetPenBack, SetPenFore will remove the "ByClass" attribute of the FILL as well. Remember to parse for it and restore it.

## Examples
```pascal
if arcLineH <> NIl then GetPenFore( arcLineH, red, green, blue ) ELSE GetPenFore( arrowLineH, red, green, blue );
SetPenFore( CNH, red, green, blue );}
{set Callout PenBack from the TextNote Group PenBack}
if arcLineH <> NIl then GetPenBack( arcLineH, red, green, blue ) ELSE GetPenBack( arrowLineH, red, green, blue );
SetPenBack( CNH, red, green, blue );

BEGIN
GetPenBack(ActiveParmHand,colorR, colorG, colorB);
SetPenBack(h,colorR, colorG, colorB);
GetPenFore(ActiveParmHand,colorR, colorG, colorB);
SetPenFore(h,colorR, colorG, colorB);
END;

GetClPenBack( kModifierClass, cR, cG, cB );
SetPenBack( h4, cR, cG, cB );
GetClPenFore( kModifierClass, cR, cG, cB );
SetPenFore( h4, cR, cG, cB );
SetFPat(h4, 0);
```
```python
colorR, colorG, colorB = vs.GetPenBack( gObjHandle )
vs.SetPenBack( hTmpHand, ( colorR, colorG, colorB ) )

vs.SetFillBack(objH, vs.GetFillBack(parentH))
vs.SetFillFore(objH, vs.GetFillFore(parentH))
vs.SetPenBack(objH, vs.GetPenBack(parentH))
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
vs.SetMarker(objH, start, end, style, size)
vs.SetOpacity(objH, vs.GetOpacity(parentH))
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
