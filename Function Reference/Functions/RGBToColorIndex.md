# RGBToColorIndex

## Description
Procedure RGBToColorIndex converts the VectorWorks palette colors from its' red, green, and blue component values to the colors' palette position index. Parameters red, green, and blue return the color components of the swatch, and parameter color is the palette position ID of the color swatch. RGB values are in the range of 0~65535. 

A color table listing with associated index values can be found in the [Script Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#color-palette).

```pascal
PROCEDURE RGBToColorIndex(
				red       : LONGINT;
				green     : LONGINT;
				blue      : LONGINT;
				VAR color : INTEGER);
```

```python
def vs.RGBToColorIndex(red, green, blue):
    return color
```

## Parameters
|Name|Type|Description|
|---|---|---|
|red|LONGINT|RGB color component value.|
|green|LONGINT|RGB color component value.|
|blue|LONGINT|RGB color component value.|
|color|INTEGER|Color index.|

## Remarks
See &lt;a href=http://www.vectorlab.info/index.php?title=Colors_in_VectorWorks_2008%2B&gt;VectorLab&lt;/a&gt; for more info on color indices in VectorWorks 2008.

## Examples
[SelectandDelObjects](examples/SelectandDelObjects.md)

## See Also
Functions:
* [ColorIndexToRGB](ColorIndexToRGB.md)
* [ColorIndexToRGBN](ColorIndexToRGBN.md)
* [RGBToColorIndexN](RGBToColorIndexN.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Utility](../Categories/Utility.md)
