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

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
