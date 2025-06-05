# ColorIndexToRGBN

## Description
Procedure ColorIndexToRGBN converts the Vectorworks palette colors from the colors' palette position index to its red, green, and blue component values. 

RGB values are in the range of 0~65535. (Black: (0, 0, 0), White: (65535, 65535, 65535))<br />
Parameter ignoreBlackBackground specifies whether the black background preference should be ignored.<br />
If set to TRUE, black and white indexes will not be inverted in black background.<br />

A color table listing with associated index values can be found in the #Color_Palette| Appendix]].

```pascal
PROCEDURE ColorIndexToRGBN(
				color                 : INTEGER;
				VAR red               : LONGINT;
				VAR green             : LONGINT;
				VAR blue              : LONGINT;
				ignoreBlackBackground : BOOLEAN);
```

```python
def vs.ColorIndexToRGBN(color, ignoreBlackBackground):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|color|INTEGER|Color index|
|red|LONGINT|RGB color component value.|
|green|LONGINT|RGB color component value.|
|blue|LONGINT|RGB color component value.|
|ignoreBlackBackground|BOOLEAN|Ignore black background preference setting or not.|

## Examples
```pascal
ColorIndexToRGBN(255,r,g,b,TRUE);
{returns the color value components of the color index 255 (black 0, 0, 0)}
{Because ignoreBlackBackground is set to TRUE, the result }
{will always be black RGB color regardless of the black background }{preference setting.}
```

## See Also
Functions:
* [ColorIndexToRGB| ColorIndexToRGB](ColorIndexToRGB|%20ColorIndexToRGB.md)
* [RGBToColorIndex| RGBToColorIndex](RGBToColorIndex|%20RGBToColorIndex.md)
* [RGBToColorIndexN| RGBToColorIndexN](RGBToColorIndexN|%20RGBToColorIndexN.md)
* [GetPenFore](GetPenFore.md) | [GetPenBack](GetPenBack.md)| [GetFillFore](GetFillFore.md) | [GetFillBack](GetFillBack.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Utility](../Categories/Utility.md)
