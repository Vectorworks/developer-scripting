# SetClFillBack

## Description
Sets the fill background color of the specified class. The color must be specified using the RGB components of the desired color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetClFillBack(
				className : STRING;
				r,g,b     : LONGINT);
```

```python
def vs.SetClFillBack(className, r,g,b):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|color|LONGINT|RGB color value. In Python, the RGB value must be passed in as tuple. See the example below.|

## Remarks
Changes the fill background color setting of the class named className.

## Examples
#### VectorScript ####
```pascal
ColorIndexToRGB(98,cRed,cGrn,cBlu);
SetClFillBack('Grassy Cover',cRed,cGrn,cBlu);
```
#### Python ####
```python
cRed,cGrn,cBlu = ColorIndexToRGB(98)
SetClFillBack('Grassy Cover',(cRed,cGrn,cBlu))

# or work with the tuple result directy
clr = ColorIndexToRGB(98)
SetClFillBack('Grassy Cover', clr)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
