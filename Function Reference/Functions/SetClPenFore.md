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

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
