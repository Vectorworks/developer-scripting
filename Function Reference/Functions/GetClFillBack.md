# GetClFillBack

## Description
Returns the fill background color setting of the specified class. The color is returned as the three RGB components of the color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetClFillBack(
				className   : STRING;
				VAR colorRV : LONGINT;
				VAR colorGV : LONGINT;
				VAR colorBV : LONGINT);
```

```python
def vs.GetClFillBack(className):
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
Returns the fill background color setting of the class named className in parameters colorRV, colorGV, and colorBV.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
   cRed, cGrn, cBlu : LONGINT;
   colorValue : INTEGER;
BEGIN
  GetClFillBack('Grassy Cover',cRed,cGrn,cBlu);
  RGBToColorIndex(cRed,cGrn,cBlu,colorValue);
  Message(colorValue);
END;
RUN(Example);
```
#### Python ####
#### Python ####
```python

```

```pascal
END;
IF (ok) & (fillbackDo) & (fillbackVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsFillColorByClass(h)
			THEN GetClFillBack(GetClass(h), r, g, b)
			ELSE GetFillBack(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(fillbackVa);
		ok := (ok) & (((fillbackOp = '=' ) & (num1 =  num2)) |
		              ((fillbackOp = '<' ) & (num1 <  num2)) |

GetClFillBack( kModifierClass, cR, cG, cB );
SetFillBack( h4, cR, cG, cB );
GetClFillFore( kModifierClass, cR, cG, cB );
SetFillFore( h4, cR, cG, cB );

GetClFillBack (UserClassName, r, g, b);
RGBToColorIndex (r, g, b, tempLongInt);
IF DecimalToColorIndex (TmpClassInfo.FillBack) <> tempLongInt THEN
	SetClFillBack (UserClassName, DecimalToColorIndex (TmpClassInfo.FillBack));
```
```python
result = vs.GetClFillBack('Wall')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
