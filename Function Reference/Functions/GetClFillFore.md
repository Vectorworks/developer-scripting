# GetClFillFore

## Description
Returns the fill foreground color setting of the specified class. The color is returned as the RGB components of the color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetClFillFore(
				className   : STRING;
				VAR colorRV : LONGINT;
				VAR colorGV : LONGINT;
				VAR colorBV : LONGINT);
```

```python
def vs.GetClFillFore(className):
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
Returns the fill foreground color setting of the class named className in parameters colorRV, colorGV, and colorBV.

## Examples
#### VectorScript ####
```pascal
GetClFillFore('Grassy Cover',cRed,cGrn,cBlu);
RGBToColorIndex(cRed,cGrn,cBlu,colorValue);
```
#### Python ####
```python
cRed,cGrn,cBlu = vs.GetClFillFore('Grassy Cover')
colorValue = vs.RGBToColorIndex(cRed,cGrn,cBlu)
```

```pascal
END;
IF (ok) & (fillforeDo) & (fillforeVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsFillColorByClass(h)
			THEN GetClFillFore(GetClass(h), r, g, b)
			ELSE GetFillFore(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(fillforeVa);
		ok := (ok) & (((fillforeOp = '=' ) & (num1 =  num2)) |
		              ((fillforeOp = '<' ) & (num1 <  num2)) |

GetClFillBack( kModifierClass, cR, cG, cB );
SetFillBack( h4, cR, cG, cB );
GetClFillFore( kModifierClass, cR, cG, cB );
SetFillFore( h4, cR, cG, cB );

GetClFillFore (UserClassName, r, g, b);
RGBToColorIndex (r, g, b, tempLongInt);
IF DecimalToColorIndex (TmpClassInfo.FillFore) <> tempLongInt THEN
	SetClFillFore (UserClassName, DecimalToColorIndex (TmpClassInfo.FillFore));
```
```python
import vs

# Returns the fill foreground color setting of the specified class.
className = 'None'

colorRV, colorGV, colorBV = vs.GetClFillFore(className)
vs.Message('GetClFillFore returned: ' + str((colorRV, colorGV, colorBV)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
