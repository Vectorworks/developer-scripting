# GetClPenBack

## Description
Returns the pen background color setting of the specified class. The color is returned as the three RGB components of the color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetClPenBack(
				className   : STRING;
				VAR colorRV : LONGINT;
				VAR colorGV : LONGINT;
				VAR colorBV : LONGINT);
```

```python
def vs.GetClPenBack(className):
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
Returns the pen background color setting of the class named className in parameters colorRV, colorGV, and colorBV.

## Examples
```pascal
END;
IF (ok) & (penbackDo) & (penbackVa <> mT) THEN BEGIN
	if false then ok := false else BEGIN
		IF IsPenColorByClass(h)
			THEN GetClPenBack(GetClass(h), r, g, b)
			ELSE GetPenBack(h, r, g, b);
		RGBToColorIndex(r, g, b, num1);
		num2 := Str2Num(penbackVa);
		ok := (ok) & (((penbackOp = '=' ) & (num1 =  num2)) |
		              ((penbackOp = '<' ) & (num1 <  num2)) |

GetClPenBack( kModifierClass, cR, cG, cB );
SetPenBack( h4, cR, cG, cB );
GetClPenFore( kModifierClass, cR, cG, cB );
SetPenFore( h4, cR, cG, cB );
SetFPat(h4, 0);
```
```python
import vs

# Returns the pen background color setting of the specified class.
className = 'None'

colorRV, colorGV, colorBV = vs.GetClPenBack(className)
vs.Message('GetClPenBack returned: ' + str((colorRV, colorGV, colorBV)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
