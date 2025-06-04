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

## See Also
VS Functions:
[GetLayerElevation](GetLayerElevation.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Layers](../Categories/Layers.md)
