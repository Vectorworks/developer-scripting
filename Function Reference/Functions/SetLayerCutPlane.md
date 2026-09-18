# SetLayerCutPlane

## Description
Sets the cut plane of the layer.

```pascal
PROCEDURE SetLayerCutPlane(
				layer    : HANDLE;
				cutPlane : REAL (Coordinate));
```

```python
def vs.SetLayerCutPlane(layer, cutPlane):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The layer.|
|cutPlane|REAL (Coordinate)|The cut plane.|

## Examples
```pascal
SetLayerCutPlane(layer, 1.0);
```
```python
import vs

# Sets the cut plane of the layer.
layer = vs.ActLayer()  # handle to the active design layer
cutPlane = 1.0

vs.SetLayerCutPlane(layer, cutPlane)
```

## See Also
VS Functions:
[GetLayerCutPlane](GetLayerCutPlane.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Layers](../Categories/Layers.md)
