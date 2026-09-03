# GetLayerCutPlane

## Description
Gets the cut plane of the layer.

```pascal
FUNCTION GetLayerCutPlane(layer : HANDLE): REAL;
```

```python
def vs.GetLayerCutPlane(layer):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The layer.|

## Examples
```pascal
resultVal := GetLayerCutPlane(layer);
```
```python
import vs

# Gets the cut plane of the layer.
layer = vs.ActLayer()  # handle to the active design layer

value = vs.GetLayerCutPlane(layer)
vs.Message('GetLayerCutPlane returned: ' + str(value))
```

## See Also
VS Functions:
[SetLayerCutPlane](SetLayerCutPlane.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Layers](../Categories/Layers.md)
