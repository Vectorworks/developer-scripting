# IsUserColor

## Description
Returns True if the color is a user color.

```pascal
FUNCTION IsUserColor(
				ColorIDX      : INTEGER;
				VAR ColorName : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.IsUserColor(ColorIDX):
    return (BOOLEAN, ColorName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ColorIDX|INTEGER|   |
|ColorName|DYNARRAY[] of CHAR|   |

## Remarks
ColorName returns the name of the color associated with the ColorIDX

## Examples
==== VectorScript ====
```pascal
PROCEDURE PaintTagWorking;
VAR
obHd : HANDLE;
x, y : REAL;
colorIDX :INTEGER;
colorName : DYNARRAY[] of CHAR;
ok : BOOLEAN;
red, green, blue : LONGINT;

BEGIN
obHd := LSActLayer;
Allocate ColorName[1..32767];
WHILE NOT(obHd=NIL) DO BEGIN
GetFillBack(obHd, red, green, blue);
RGBToColorIndex(red, green, blue, colorIDX);
ok := IsUserColor(colorIDX, colorName);
IF ok THEN BEGIN
HCenter(obHd, x, y);
TextOrigin(x, y);
CreateText(colorName);
END;
obHd := PrevSObj(obHd);
END;
END;
RUN(PaintTagWorking);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
