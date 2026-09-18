# SetClPenBack

## Description
Procedure SetClPenBack sets the pen background color of the specified class. The color must be specified using the RGB components of the desired color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetClPenBack(
				className : STRING;
				r,g,b     : LONGINT);
```

```python
def vs.SetClPenBack(className, r,g,b):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|color|LONGINT|RGB color value.|

## Remarks
Changes the pen background color setting of the class named className.

## Examples
#### VectorScript ####
```pascal
ColorIndexToRGB(214,cRed,cGrn,cBlu);
SetClPenBack('Cold Water Supply',cRed,cGrn,cBlu);
```
#### Python ####
```python

```

```pascal
NameClass(sprayClass);
SetClFillFore(sprayClass, 0, 0, 0);
SetClFillBack(sprayClass, 577, 43860, 60159);
SetClPenFore(sprayClass, 577, 43860, 60159);
SetClPenBack(sprayClass, 65535, 65535, 65535);
SetClFPat(sprayClass, 1);
SetClLSN(sprayClass, 2);
SetClLW(sprayClass, 1);
SetClUseGraphic(sprayClass, TRUE);

NameClass( modifierClass ); { to create if not yet existing }
SetClFillFore( modifierClass,0,0,0);
SetClFillBack( modifierClass,65535,65535,65535);
SetClPenFore( modifierClass,577,43860,60159); {** This gives the distinctive blue color for the control fence.}
SetClPenBack( modifierClass,65535,65535,65535);
SetClFPat( modifierClass, 0);
SetClLSN( modifierClass, CheckLSN(-6));
SetClLW( modifierClass, 1);
SetClUseGraphic( modifierClass,TRUE);

END;
if GetType(classHandle) = 94 then BEGIN
	SetClFillFore  (modifierClass,     0,     0,     0);
	SetClFillBack  (modifierClass, 65535, 65535, 65535);
	SetClPenBack   (modifierClass, 65535, 65535, 65535);
	SetClPenFore   (modifierClass,   577, 43860, 60159); {control fence blue}
	SetClFPat      (modifierClass, 0);
	SetClLSN       (modifierClass,CheckLSN(-6));
	SetClLW        (modifierClass, 1);
```
```python
vs.SetClPenBack('Wall', r, g, b)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
