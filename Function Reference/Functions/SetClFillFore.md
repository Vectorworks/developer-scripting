# SetClFillFore

## Description
Sets the fill foreground color of the specified class. The color must be specified using the RGB components of the desired color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetClFillFore(
				className : STRING;
				r,g,b     : LONGINT);
```

```python
def vs.SetClFillFore(className, r,g,b):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|color|LONGINT|RGB color value.|

## Remarks
Changes the fill foreground color setting of the class named className.

## Examples
#### VectorScript ####
```pascal
ColorIndexToRGB(24,cRed,cGrn,cBlu);
SetClFillFore('Grassy Cover',cRed,cGrn,cBlu);
```
#### Python ####
```python

```

```pascal
GetWSCellValue (wksHand, row, col+5, tempInt);	{fill fore pen color}
ColorIndexToRGB (tempInt, r, g, b);
SetClFillFore (userClassName, r, g, b);

GetClFillFore (UserClassName, r, g, b);
RGBToColorIndex (r, g, b, tempLongInt);
IF DecimalToColorIndex (TmpClassInfo.FillFore) <> tempLongInt THEN
	SetClFillFore (UserClassName, DecimalToColorIndex (TmpClassInfo.FillFore));

SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
SetClLW (UserClassName, TmpClassInfo.LW);
SetClLSN (UserClassName, TmpClassInfo.LS);
SetClFPat (UserClassName, TmpClassInfo.FillPat);
SetClFillFore (UserClassName, DecimalToColorIndex (TmpClassInfo.FillFore));
SetClFillBack (UserClassName, DecimalToColorIndex (TmpClassInfo.FillBack));
SetClUseGraphic (UserClassName, TmpClassInfo.UseAtCreation);
tempH := GetObject (UserClassName);
IF tempH <> NIL THEN
```
```python
tempInt = vs.GetWSCellValue( wksHand, row, col + 5 )
# fill fore pen color
r, g, b = vs.ColorIndexToRGB( tempInt, r, g, b )
vs.SetClFillFore( userClassName, r, g, b )
tempInt = vs.GetWSCellValue( wksHand, row, col + 6 )
# fill back pen color
r, g, b = vs.ColorIndexToRGB( tempInt, r, g, b )
vs.SetClFillBack( userClassName, r, g, b )
```
See also in tutorials: [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
