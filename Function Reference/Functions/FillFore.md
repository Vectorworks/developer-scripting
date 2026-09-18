# FillFore

## Description
Procedure FillFore sets the active fill foreground color setting for the document. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FillFore(color : LONGINT);
```

```python
def vs.FillFore(color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|color|LONGINT|RGB color value to set as active fill foreground color.|

## Remarks
*\_c\_* 2015.05.19: This routine will also accept a single INTEGER Color Palette Index value in lieu of three LONGINT RGB values for the COLOR parameter. The Color index can be obtained with [RGBToColorIndex](RGBToColorIndex.md). See remarks under [SetPenFore](SetPenFore.md) for more infos. On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].

## Examples
#### VectorScript ####
```pascal
FillFore(65535, 0, 39321); { using RGB values }

colorIndex := RGBToColorIndex(65535, 0, 39321);
FillFore(colorIndex); { using Color Index values }
```
#### Python ####
```python
vs.FillFore((65535, 0, 39321)) # using RGB values

colorIndex = vs.RGBToColorIndex(65535, 0, 39321)
vs.FillFore(colorIndex) # using Color Index values
```

```pascal
ResetFillStyle(TempH);
SetLW(TempH,gGypLW);
PenSize(gStippleLW);
ColorIndexToRGB(gStippleFill,Red,Green,Blue);
FillFore(Red,Green,Blue);
FillBack(Red,Green,Blue);
ColorIndexToRGB(gStippleColor,Red,Green,Blue);
PenFore(Red,Green,Blue);
PenBack(Red,Green,Blue);

if not IsFillColorByClass(objHand) then BEGIN
	GetFillFore(objHand, red, green, blue);
	FillFore(red, green, blue);
	GetFillBack(objHand, red, green, blue);
	FillBack(red, green, blue);
END;

BEGIN
	FillPat (JoistFillPattern );
	FillFore(JoistFillFore );
	FillBack(JoistFillBack);
END;
```
```python
if not vs.IsFillColorByClass( objHand ):
	rgb = vs.GetFillFore( objHand )
	vs.FillFore( rgb )
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md)

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
