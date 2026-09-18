# GetMtlPenBackColor

## Description
Returns the pen background color of the specified material. The color is returned as the RGB components of the color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetMtlPenBackColor(
				material  : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetMtlPenBackColor(material):
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
Returns the pen background color of the material in parameters colorRV, colorGV, and colorBV.

## Examples
```python
GetMtlPenBackColor(mtlHandle,cRed,cGrn,cBlu);
RGBToColorIndex(cRed,cGrn,cBlu,colorValue);
```

```pascal
GetMtlPenBackColor(material, 1, 2, 3);
```
```python
import vs

# Returns the pen background color of the specified material.
material = vs.FSActLayer()  # handle to the first selected object on the active layer

red, green, blue = vs.GetMtlPenBackColor(material)
vs.Message('GetMtlPenBackColor returned: ' + str((red, green, blue)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
