# PenFore

## Description
Procedure PenFore sets the active pen foreground color for the document. RGB values are in the range of 0~65535.

```pascal
PROCEDURE PenFore(color : LONGINT);
```

```python
def vs.PenFore(color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|color|LONGINT|RGB color value to be set as active pen foreground.|

## Remarks
*\_c\_* 2015.05.19: This Procedure will also accept a single INTEGER Color Palette Index value in lieu of three LONGINT RGB values for the COLOR parameter. The Color index can be obtained with [RGBToColorIndex](RGBToColorIndex.md). See remarks under [SetPenFore](SetPenFore.md) for more infos. On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].

When using this command, you should check for the black background preference setting if you're trying to draw black lines.

## Examples
#### VectorScript ####
```pascal
PenFore(65535, 0, 39321); { using RGB values }

colorIndex := RGBToColorIndex(65535, 0, 39321);
PenFore(colorIndex); { using Color Index values }
```
#### Python ####
```python
vs.PenFore((65535, 0, 39321)) # using RGB values

colorIndex = vs.RGBToColorIndex(65535, 0, 39321)
vs.PenFore(colorIndex) # using Color Index values
```

```pascal
BEGIN
	GetPenFore (gWallHand,r,g,b);
	PenFore (r,g,b);
	Pensize (GetLW (gWallHand));
	PenPatN (GetLSN (gWallHand));
	GetFillBack (gWallHand,r,g,b);
	FillBack (r,g,b);

Options[1] := 'Spotlight'; {Saved xml Category}
Options[2] := 'SeatingLayoutPick'; {Saved xml Item}
Options[3] := ''; {Check Box String}
AlertInformDontShowAgain(GetPlugInString(3010),'', FALSE, Options);
PenFore(45000, 45000, 45000);
SetPref(9871, TRUE);
GetOrigin(OriginX,OriginY);
Is3dView := GetProjection(ActLayer)<>6;
RunTempTool(TempToolCallback, TRUE);

FPenFore(saveR, saveG, saveB);
PenPatN(gLeaderType);
PenSize(gLeaderThickness);
GetPenFore(ActiveParmHand, r, g, b);
PenFore(r, g, b);
MoveTo(bubbleIntPt.x, bubbleIntPt.y);
LineTo(shoulderPt.x, shoulderPt.y);
LineTo(markerPt.x, markerPt.y);
PenPatN(savePenPat);
```
```python
if not vs.IsPenColorByClass( objHand ):
	rgb = vs.GetPenFore( objHand )
	vs.PenFore( rgb )
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
