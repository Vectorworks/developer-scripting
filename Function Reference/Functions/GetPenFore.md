# GetPenFore

## Description
Procedure GetPenFore returns the pen foreground color components of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetPenFore(
				h         : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetPenFore(h):
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
GetPenFore(handleToObject,redValue,greenValue,blueValue);
```
#### Python ####
```python
red_value, green_value, blue_value = vs.GetPenFore(handleToObject)
```

## See Also
VS Functions: [ColorIndexToRGB](ColorIndexToRGB.md) | [RGBToColorIndex](RGBToColorIndex.md) | [GetPenBack](GetPenBack.md) | [GetFillFore](GetFillFore.md) | [GetFillBack](GetFillBack.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
