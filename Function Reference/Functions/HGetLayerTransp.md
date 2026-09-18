# HGetLayerTransp

## Description
Get the transparency of the specified layer.

```pascal
FUNCTION HGetLayerTransp(hLayer : HANDLE): REAL;
```

```python
def vs.HGetLayerTransp(hLayer):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|Handle to the layer.|

## Examples
```pascal
resultVal := HGetLayerTransp(hLayer);
```
```python
import vs

# Get the transparency of the specified layer.
hLayer = vs.ActLayer()  # handle to the active design layer

value = vs.HGetLayerTransp(hLayer)
vs.Message('HGetLayerTransp returned: ' + str(value))
```

## See Also
VS Functions:
[HSetLayerTransp](HSetLayerTransp.md) 
| [GetLayerTransparency](GetLayerTransparency.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Layers](../Categories/Layers.md)
