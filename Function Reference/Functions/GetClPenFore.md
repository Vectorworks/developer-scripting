# GetClPenFore

## Description
Returns the pen foreground color setting of the specified class. The color is returned as the three RGB components of the color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetClPenFore(
				className   : STRING;
				VAR colorRV : LONGINT;
				VAR colorGV : LONGINT;
				VAR colorBV : LONGINT);
```

```python
def vs.GetClPenFore(className):
    return (colorRV, colorGV, colorBV)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|colorRV|LONGINT|Returns RGB color component (red).|
|colorGV|LONGINT|Returns RGB color component (green).|
|colorBV|LONGINT|Returns RGB color component (blue).|

## Remarks
Returns the pen foreground color setting of the class named className in parameters colorRV, colorGV, and colorBV.

## Examples
#### VectorScript ####
```pascal
GetClPenFore('Grassy Cover',cRed,cGrn,cBlu);
RGBToColorIndex(cRed,cGrn,cBlu,colorValue);
```
#### Python ####
```python
cRed,cGrn,cBlu = vs.GetClPenFore('Grassy Cover')
colorValue = vs.RGBToColorIndex(cRed,cGrn,cBlu)
```

```pascal
END;
IF (ok) & (penforeDo) & (penforeVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsPenColorByClass(h)
			THEN GetClPenFore(GetClass(h), r, g, b)
			ELSE GetPenFore(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(penforeVa);
		ok := (ok) & (((penforeOp = '=' ) & (num1 =  num2)) |
		              ((penforeOp = '<' ) & (num1 <  num2)) |

GetClPenBack( kModifierClass, cR, cG, cB );
SetPenBack( h4, cR, cG, cB );
GetClPenFore( kModifierClass, cR, cG, cB );
SetPenFore( h4, cR, cG, cB );
SetFPat(h4, 0);

GetClPenFore (UserClassName, r, g, b);
RGBToColorIndex (r, g, b, tempLongInt);
IF DecimalToColorIndex (TmpClassInfo.PenColor) <> tempLongInt THEN
	SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
```
```python
import vs

# Returns the pen foreground color setting of the specified class.
className = 'None'

colorRV, colorGV, colorBV = vs.GetClPenFore(className)
vs.Message('GetClPenFore returned: ' + str((colorRV, colorGV, colorBV)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
