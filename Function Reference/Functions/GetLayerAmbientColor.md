# GetLayerAmbientColor

## Description
Procedure GetLayerAmbientColor returns the color of the ambient light of the referenced layer. RGB values are in the range of 0~65535.

```pascal
PROCEDURE GetLayerAmbientColor(
				layer     : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetLayerAmbientColor(layer):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|Handle to layer.|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
