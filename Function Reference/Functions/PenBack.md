# PenBack

## Description
Procedure PenBack set the active pen background color for the document. RGB values are in the range of 0~65535.

```pascal
PROCEDURE PenBack(color : LONGINT);
```

```python
def vs.PenBack(color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|color|LONGINT|RGB color value to be set as active pen background.|

## Remarks
*_c_* 2015.05.19: This Procedure will also accept a single INTEGER Color Palette Index value in lieu of three LONGINT RGB values for the COLOR parameter. The Color index can be obtained with [[VS:RGBToColorIndex]]. See remarks under [[VS:SetPenFore]] for more infos. On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].

## Examples
#### VectorScript ####
```pascal
PenBack(65535, 0, 39321); { using RGB values }

colorIndex := RGBToColorIndex(65535, 0, 39321);
PenBack(colorIndex); { using Color Index values }
```
#### Python ####
```python
vs.PenBack((65535, 0, 39321)) # using RGB values

colorIndex = vs.RGBToColorIndex(65535, 0, 39321)
vs.PenBack(colorIndex) # using Color Index values
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
