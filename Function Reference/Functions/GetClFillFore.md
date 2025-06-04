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
==== VectorScript ====
```pascal
GetClFillFore('Grassy Cover',cRed,cGrn,cBlu);
RGBToColorIndex(cRed,cGrn,cBlu,colorValue);
```
==== Python ====
```python
cRed,cGrn,cBlu = vs.GetClFillFore('Grassy Cover')
colorValue = vs.RGBToColorIndex(cRed,cGrn,cBlu)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
