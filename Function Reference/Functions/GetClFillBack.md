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
==== VectorScript ====
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
==== Python ====
==== Python ====
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
