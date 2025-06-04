# RGBToColorIndexN

## Description
Procedure RGBToColorIndexN converts the Vectorworks palette colors from its' red, green, and blue component values to the Vectorworks color index. Parameters red, green, and blue return the color components of the swatch, and parameter color is the Vectorworks color index. RGB values are in the range of 0~65535. Parameter ignoreBlackBackground specifies whether the black background preference should be ignored. If set to TRUE, black and white indexes will not be inverted in black background.

A color table listing with associated index values can be found in the [[VS:Function_Reference_Appendix#Color_Palette| Appendix]].

```pascal
PROCEDURE RGBToColorIndexN(
				red                   : LONGINT;
				green                 : LONGINT;
				blue                  : LONGINT;
				VAR color             : INTEGER;
				ignoreBlackBackground : BOOLEAN);
```

```python
def vs.RGBToColorIndexN(red, green, blue, ignoreBlackBackground):
    return color
```

## Parameters
|Name|Type|Description|
|---|---|---|
|red|LONGINT|RGB color component value.|
|green|LONGINT|RGB color component value.|
|blue|LONGINT|RGB color component value.|
|color|INTEGER|Color index.|
|ignoreBlackBackground|BOOLEAN|Ignore black background preference setting or not.|

## Examples
==== Pascal ====
```pascal
PROCEDURE Example;
VAR
	red, green, blue :LONGINT;
	colorIndex :INTEGER;
BEGIN
	GetPenFore(FSActLayer, red, green, blue);
	RGBToColorIndexN(red, green, blue, colorIndex, TRUE);
	Message(colorIndex);
END;
RUN(Example)
```
==== Python ====
```python
# (_c_ 2024.04.19):
# create Autocad colors with their index as name. Upon importing them from DWG, the colors have a slight shift compared to the original RGB values
# and there is no way to control this in the settings
# this scripts creates the true Autocad colours according to this source:
# Source: https://gohtx.com/acadcolors.php
# you can then save them in a dedicated palette

# list of: index, r, g, b
# Warning: this is not the complete list! Only indexes 0-10, as representation of the system
# Please see Discussion for copy pasting the full list of RGB values
colorData = [[0, 0, 0, 0], [1, 255, 0, 0], [2, 255, 255, 0], [3, 0, 255, 0], [4, 0, 255, 255], [5, 0, 0, 255], [6, 255, 0, 255], [7, 255, 255, 255], [8, 65, 65, 65], [9, 128, 128, 128], [10, 255, 0, 0]] 

def longInt(i):
	return vs.Min(i * 257, 65535)

results =""
for c in colorData:
	i = vs.RGBToColorIndexN(longInt(c[1]), longInt(c[2]), longInt(c[3]), True)
	ok = vs.SetColorName(i, str(c[0])) # use the index as the color name, this makes their usage later much easier

	if ok == False:
		results = f"{results}\r{c[0]} Failed: {c[1]}, {c[2]}, {c[3]}" # they fail if the color is already in the current doc
vs.AlrtDialog(results)
```

## See Also
Functions:
* [ColorIndexToRGB| ColorIndexToRGB](ColorIndexToRGB|%20ColorIndexToRGB.md)
* [ColorIndexToRGBN| ColorIndexToRGBN](ColorIndexToRGBN|%20ColorIndexToRGBN.md)
* [RGBToColorIndex| RGBToColorIndex](RGBToColorIndex|%20RGBToColorIndex.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Utility](../Categories/Utility.md)
