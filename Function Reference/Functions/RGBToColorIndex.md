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

## Examples
[SelectandDelObjects](examples/SelectandDelObjects.md)

```pascal
if false then ok := false else BEGIN
	IF IsFillColorByClass(h)
		THEN GetClFillBack(GetClass(h), r, g, b)
		ELSE GetFillBack(h, r, g, b);
	RGBToColorIndex(r, g, b, num1);
	num2 := Str2Num(fillbackVa);
	ok := (ok) & (((fillbackOp = '=' ) & (num1 =  num2)) |
	              ((fillbackOp = '<' ) & (num1 <  num2)) |
	              ((fillbackOp = '>' ) & (num1 >  num2)) |

BEGIN
	IF caller = kComponentsSymbol THEN BEGIN
		{ get background color and decide what the color for components in 'Flights and Platforms' tab should be. BS, 10/12/2007. }
		FFillBack( rc, gc, bc );
		RGBToColorIndex( rc, gc, bc, backColor );
		IF backColor = 0 THEN compColor := 255
		ELSE compColor := 257;

		END; {of CASE}
	temp_s := '';
	temp_i := temp_i + 1;
	END;
RGBToColorIndex(R,G,B,colidx);
ColorVar2Index := colidx;
END;
```
```python
import vs

# Procedure RGBToColorIndex converts the VectorWorks palette colors from its'
# red, green, and blue component values to the colors' palette position index.
red = 65535
green = 0
blue = 0

result = vs.RGBToColorIndex(red, green, blue)
```

## See Also
Functions:
* [ColorIndexToRGB](ColorIndexToRGB.md)
* [ColorIndexToRGBN](ColorIndexToRGBN.md)
* [RGBToColorIndexN](RGBToColorIndexN.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Utility](../Categories/Utility.md)
