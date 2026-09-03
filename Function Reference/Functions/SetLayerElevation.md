# SetLayerElevation

## Description
Sets the elevation and thickness of the specified layer.

```pascal
PROCEDURE SetLayerElevation(
				h         : HANDLE;
				baseElev  : REAL;
				thickness : REAL);
```

```python
def vs.SetLayerElevation(h, baseElev, thickness):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the layer|
|baseElev|REAL|Base elevation of the layer|
|thickness|REAL|Thickness of the layer|

## Examples
```pascal
SetLayerElevation(h, 1.0, 2.0);
```
```python
import vs

# Sets the elevation and thickness of the specified layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
baseElev = 0.0
thickness = 0.1

vs.SetLayerElevation(h, baseElev, thickness)
```

## See Also
VS Functions:
[GetLayerElevation](GetLayerElevation.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Layers](../Categories/Layers.md)
