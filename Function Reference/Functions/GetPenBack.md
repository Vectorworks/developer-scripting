# GetPenBack

## Description
Procedure GetPenBack returns the pen (pattern) background color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetPenBack(
				h         : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetPenBack(h):
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
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
r, g, b :LONGINT;
BEGIN
h := FSActLayer;
GetPenBack(h, r, g, b);
Message('r= ', r, ' g= ', g, ' b= ', b);
END;
RUN(Example);
```
==== Python ====
```python
def example():
	h = vs.FSActLayer()
	r, g, b = vs.GetPenBack(h)
	vs.Message('r= ', r, ' g= ', g, ' b= ', b)

example()
```

## See Also
VS Functions: [RGBToColorIndex](RGBToColorIndex.md) | [ColorIndexToRGB](ColorIndexToRGB.md) | [GetFillFore](GetFillFore.md) | [GetFillBack](GetFillBack.md) | [GetPenFore](GetPenFore.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
