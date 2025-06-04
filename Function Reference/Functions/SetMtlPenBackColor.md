# SetMtlPenBackColor

## Description
Sets the pen background color of the specified material. The color must be specified using the RGB components of the desired color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetMtlPenBackColor(
				material : HANDLE;
				color    : LONGINT);
```

```python
def vs.SetMtlPenBackColor(material, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|material|HANDLE|Handle to material.|
|color|LONGINT|RGB color value.|

## Remarks
Sets the pen background color of the material.

## Examples
```python
ColorIndexToRGB(214,cRed,cGrn,cBlu);
SetMtlPenBackColor(mtlHandle,cRed,cGrn,cBlu);
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
