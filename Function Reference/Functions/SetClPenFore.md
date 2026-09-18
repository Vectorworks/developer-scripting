# SetClPenFore

## Description
Sets the pen foreground color of the specified class. The color must be specified using the RGB components of the desired color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetClPenFore(
				className : STRING;
				r,g,b     : LONGINT);
```

```python
def vs.SetClPenFore(className, r,g,b):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|color|LONGINT|RGB color value.|

## Remarks
Changes the pen foreground color setting of the class named className.

## Examples
#### VectorScript ####
```pascal
ColorIndexToRGB(214,cRed,cGrn,cBlu);
SetClPenFore('Cold Water Supply',cRed,cGrn,cBlu);
```
#### Python ####
```python

```

```pascal
BEGIN
	GetWSCellValue (wksHand, row, col+1, tempInt);	{pen color}
	ColorIndexToRGB (tempInt, r, g, b);
	SetClPenFore (userClassName, r, g, b);

GetClPenFore (UserClassName, r, g, b);
RGBToColorIndex (r, g, b, tempLongInt);
IF DecimalToColorIndex (TmpClassInfo.PenColor) <> tempLongInt THEN
	SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));

BEGIN
	NameClass (UserClassName);
	SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
	SetClLW (UserClassName, TmpClassInfo.LW);
	SetClLSN (UserClassName, TmpClassInfo.LS);
	SetClFPat (UserClassName, TmpClassInfo.FillPat);
	SetClFillFore (UserClassName, DecimalToColorIndex (TmpClassInfo.FillFore));
```
```python
tempInt = vs.GetWSCellValue( wksHand, row, col + 1 )
# pen color
r, g, b = vs.ColorIndexToRGB( tempInt )
vs.SetClPenFore( userClassName, r, g, b )
tempInt = vs.GetWSCellValue( wksHand, row, col + 2 )
# line weight
vs.SetClLW( userClassName, tempInt )
tempInt = vs.GetWSCellValue( wksHand, row, col + 3 )
```
See also in tutorials: [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
