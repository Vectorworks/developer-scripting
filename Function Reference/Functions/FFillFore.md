# FFillFore

## Description
Procedure FFillFore returns the current fill foreground color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FFillFore(
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.FFillFore():
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
FFillFore(redValue,greenValue,blueValue);
```
==== Python ====
```python
redValue,greenValue,blueValue = vs.FFillFore()
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
