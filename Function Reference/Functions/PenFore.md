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

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
