# HSetLayerTransp

## Description
Set the transparency of the specified layer.

```pascal
PROCEDURE HSetLayerTransp(
				hLayer       : HANDLE;
				transparency : REAL);
```

```python
def vs.HSetLayerTransp(hLayer, transparency):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|Handle to the layer.|
|transparency|REAL|The transparency for the layer. Value between 0.0 and 100.0|

## Examples
```pascal
HSetLayerTransp(hLayer, 1.0);
```
```python
import vs

# Set the transparency of the specified layer.
hLayer = vs.ActLayer()  # handle to the active design layer
transparency = 1.0

vs.HSetLayerTransp(hLayer, transparency)
```

## See Also
VS Functions:
[SetLayerTransparency](SetLayerTransparency.md) 
| [HGetLayerTransp](HGetLayerTransp.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Layers](../Categories/Layers.md)
