# GetLayerAmbientInfo

## Description
Procedure GetLayerAmbientInfo returns the attribute values for the ambient light object of the referenced layer.

```pascal
PROCEDURE GetLayerAmbientInfo(
				layer          : HANDLE;
				VAR isOn       : BOOLEAN;
				VAR brightness : INTEGER);
```

```python
def vs.GetLayerAmbientInfo(layer):
    return (isOn, brightness)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|Handle to layer.|
|isOn|BOOLEAN|On-off status of ambient light.|
|brightness|INTEGER|Brightness of ambient light.|

## Remarks
brightness is a percentage value

## Examples
```pascal
GetLayerAmbientInfo(layer, TRUE, 1);
```
```python
import vs

# Procedure GetLayerAmbientInfo returns the attribute values for the ambient
# light object of the referenced layer.
layer = vs.ActLayer()  # handle to the active design layer

isOn, brightness = vs.GetLayerAmbientInfo(layer)
vs.Message('GetLayerAmbientInfo returned: ' + str((isOn, brightness)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
