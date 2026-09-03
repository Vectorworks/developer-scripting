# SetLayerEnableCutPl

## Description
Sets whether the cut plane of the layer is enabled.

```pascal
PROCEDURE SetLayerEnableCutPl(
				layer          : HANDLE;
				enableCutPlane : BOOLEAN);
```

```python
def vs.SetLayerEnableCutPl(layer, enableCutPlane):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The layer.|
|enableCutPlane|BOOLEAN|Whether the cut plane is enabled.|

## Examples
```pascal
SetLayerEnableCutPl(layer, TRUE);
```
```python
import vs

# Sets whether the cut plane of the layer is enabled.
layer = vs.ActLayer()  # handle to the active design layer
enableCutPlane = True

vs.SetLayerEnableCutPl(layer, enableCutPlane)
```

## See Also
VS Functions:
[GetLayerEnableCutPl](GetLayerEnableCutPl.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Layers](../Categories/Layers.md)
