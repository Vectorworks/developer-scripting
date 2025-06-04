# SetLightInfo

## Description
Sets the attributes of the referenced light object.

```pascal
PROCEDURE SetLightInfo(
				h          : HANDLE;
				lightType  : INTEGER;
				brightness : INTEGER;
				isOn       : BOOLEAN;
				castShadow : BOOLEAN);
```

```python
def vs.SetLightInfo(h, lightType, brightness, isOn, castShadow):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|lightType|INTEGER|Light type.|
|brightness|INTEGER|Brightness of light.|
|isOn|BOOLEAN|On-off status of light.|
|castShadow|BOOLEAN|Shadow casting status of light.|

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
