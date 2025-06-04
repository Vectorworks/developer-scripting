# GetMtlPenForeColor

## Description
Returns the pen foreground color of the specified material. The color is returned as the RGB components of the color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetMtlPenForeColor(
				material  : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetMtlPenForeColor(material):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|material|HANDLE|Handle to material.|
|red|LONGINT|Returns RGB color component (red).|
|green|LONGINT|Returns RGB color component (green).|
|blue|LONGINT|Returns RGB color component (blue).|

## Remarks
Returns the pen foreground color setting of the material in parameters colorRV, colorGV, and colorBV.

## Examples
```python
GetMtlPenForeColor(mtlHandle,cRed,cGrn,cBlu);
RGBToColorIndex(cRed,cGrn,cBlu,colorValue);
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
