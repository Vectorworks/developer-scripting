# ColorIndexToRGB

## Description
Procedure ColorIndexToRGB converts the VectorWorks palette colors from the colors' palette position index to its red, green, and blue component values. 
RGB values are in the range of 0~65535. (Black: (0, 0, 0), White: (65535, 65535, 65535))

A color table listing with associated index values can be found in the [[VS:Function_Reference_Appendix#Color_Palette| Appendix]]

```pascal
PROCEDURE ColorIndexToRGB(
				color     : INTEGER;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.ColorIndexToRGB(color):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|color|INTEGER|Color index.|
|red|LONGINT|RGB color component value.|
|green|LONGINT|RGB color component value.|
|blue|LONGINT|RGB color component value.|

## Examples
==== VectorScript ====
```pascal
ColorIndexToRGB(45, r, g, b);
{returns the color value components of the color at position 45}
```
==== Python ====
```python
r, g, b = vs.ColorIndexToRGB(45)
```

## See Also
Functions:
* [ColorIndexToRGBN| ColorIndexToRGBN](ColorIndexToRGBN|%20ColorIndexToRGBN.md)
* [RGBToColorIndex| RGBToColorIndex](RGBToColorIndex|%20RGBToColorIndex.md)
* [RGBToColorIndexN| RGBToColorIndexN](RGBToColorIndexN|%20RGBToColorIndexN.md)
* [GetPenFore](GetPenFore.md) | [GetPenBack](GetPenBack.md)| [GetFillFore](GetFillFore.md) | [GetFillBack](GetFillBack.md)

## Version
Availability: from MiniCAD 6.0

## Category
* [Utility](../Categories/Utility.md)
