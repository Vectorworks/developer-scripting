# SetLayerElevationN

## Description
Sets the elevation and thickness of the specified layer.

```pascal
PROCEDURE SetLayerElevationN(
				h         : HANDLE;
				baseElev  : REAL;
				thickness : REAL);
```

```python
def vs.SetLayerElevationN(h, baseElev, thickness):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the layer.|
|baseElev|REAL|Base elevation of the layer in document units.|
|thickness|REAL|Thickness of the layer in document units.|

## See Also
VS Functions:
[GetLayerElevationN](GetLayerElevationN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
