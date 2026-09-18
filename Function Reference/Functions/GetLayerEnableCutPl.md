# GetLayerEnableCutPl

## Description
Gets whether the cut plane of the layer is enabled.

```pascal
FUNCTION GetLayerEnableCutPl(layer : HANDLE): BOOLEAN;
```

```python
def vs.GetLayerEnableCutPl(layer):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The layer.|

## Examples
```pascal
resultOK := GetLayerEnableCutPl(layer);
```
```python
import vs

# Gets whether the cut plane of the layer is enabled.
layer = vs.ActLayer()  # handle to the active design layer

ok = vs.GetLayerEnableCutPl(layer)
if ok:
    vs.Message('GetLayerEnableCutPl succeeded')
else:
    vs.Message('GetLayerEnableCutPl failed')
```

## See Also
VS Functions:
[SetLayerEnableCutPl](SetLayerEnableCutPl.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Layers](../Categories/Layers.md)
