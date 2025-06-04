# SetLayerAmbientInfo

## Description
Procedure SetLayerAmbientInfo sets the attribute values for the ambient light object of the referenced layer.

```pascal
PROCEDURE SetLayerAmbientInfo(
				layer      : HANDLE;
				isOn       : BOOLEAN;
				brightness : INTEGER);
```

```python
def vs.SetLayerAmbientInfo(layer, isOn, brightness):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|Handle to layer.|
|isOn|BOOLEAN|On-off status of ambient light|
|brightness|INTEGER|Brightness of ambient light.|

## Remarks
brightness is a percentage value

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
