# FFillBack

## Description
Procedure FFillBack returns the current fill background color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FFillBack(
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.FFillBack():
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Examples
==== VectorScript ====
```pascal
FFillBack(redValue,greenValue,blueValue);
```
==== Python ====
```python
redValue,greenValue,blueValue = vs.FFillBack()
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
