# SetLayerAmbientColor

## Description
Procedure SetLayerAmbientColor sets the color for the ambient light of the referenced layer. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetLayerAmbientColor(
				layer : HANDLE;
				red   : LONGINT;
				green : LONGINT;
				blue  : LONGINT);
```

```python
def vs.SetLayerAmbientColor(layer, red, green, blue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|Handle to layer.|
|red|LONGINT|RGB color component value.|
|green|LONGINT|RGB color component value.|
|blue|LONGINT|RGB color component value.|

## Examples
```pascal
SetLayerAmbientColor(layer, 1, 2, 3);
```
```python
import vs

# Procedure SetLayerAmbientColor sets the color for the ambient light of the
# referenced layer.
layer = vs.ActLayer()  # handle to the active design layer
red = 65535
green = 0
blue = 0

vs.SetLayerAmbientColor(layer, red, green, blue)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
