# FPenBack

## Description
Procedure FPenBack returns the current pen background color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FPenBack(
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.FPenBack():
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
