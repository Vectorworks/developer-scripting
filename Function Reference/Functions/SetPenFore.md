# SetPenFore

## Description
Procedure SetPenFore sets the pen foreground color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetPenFore(
				h     : HANDLE;
				color : LONGINT);
```

```python
def vs.SetPenFore(h, color):
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
*: <code>SetPenFore(FSActLayer, colorIndex);</code>
* Three RGB longints:
*: <code>SetPenFore(FSActLayer, 65535, 0, 0);</code>
 
Python:
* Singular color index:
*: <code>vs.SetPenFore(vs.FSActLayer(), vs.RGBToColorIndex(65535, 0, 0)) </code>
* Three longints in a tuple:
*: <code>vs.SetPenFore(vs.FSActLayer(), (65535, 0, 0)) </code>
* Three hex numbers in a tuple:
*: <code>vs.SetPenFore(vs.FSActLayer(), (0xFFFF, 0, 0)) </code>

On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].
; Warning: SetPenBack, SetPenFore will remove the "ByClass" attribute of the FILL as well. Remember to parse for it and restore it.

(Joel Sciamma 2006.08.14): To have no pen drawn, use SetLW to set the line weight to zero.

## Examples
[SelectandDelObjects](examples/SelectandDelObjects.md)

```pascal
LineTo(pLineLength-dx,0);
SetLSN(lnewobj,2);
SetLW(lnewobj,wid);
IF GetPref(16) THEN	{black background}
	SetPenFore(lnewobj,0,0,0)
ELSE SetPenFore(lnewobj,65535,65535,65535);
IF pFlip
	THEN Arc(0.0,pLineLength/2,pLineLength,-pLineLength/2,190,160.0)
	ELSE Arc(0.0,pLineLength/2,pLineLength,-pLineLength/2,170,-160.0);

SetRField(hobj,kRecName,kStatName,StatVal);
WHILE (hobj <> NIL) DO BEGIN
	SetPenFore(hobj,r,g,b);
	hobj := NextObj(hobj);
	END;

BEGIN
	FPenFore (R, G, B);
	SetPenFore (objectH, R, G, B);
END;
```
```python
else:
	colorR, colorG, colorB = vs.GetPenFore( gObjHandle )
	vs.SetPenFore( hTmpHand, ( colorR, colorG, colorB )	)

vs.CreateText( message1 )
vs.SetTextVerticalAlign( vs.LNewObj(), 3 )
vs.SetTextJust( vs.LNewObj(), 2 )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 0 )
b1, b2 = vs.GetBBox( vs.LNewObj() )
vs.Rect( kBf * b1[0], kBf * b1[1], kBf * b2[0], kBf * b2[1] )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )

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
