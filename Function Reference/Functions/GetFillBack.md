# GetFillBack

## Description
Procedure GetFillBack returns the fill background color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetFillBack(
				h         : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetFillBack(h):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Examples
#### VectorScript ####
```pascal
GetFillBack(handleToObject,redValue,greenValue,blueValue);
```
#### Python ####
```python
red_value, green_value, blue_value = vs.GetFillBack(vs.FSActLayer())
```

## See Also
VS Functions: [RGBToColorIndex](RGBToColorIndex.md) | [ColorIndexToRGB](ColorIndexToRGB.md) | [GetFillFore](GetFillFore.md) | [GetPenFore](GetPenFore.md) | [GetPenBack](GetPenBack.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
