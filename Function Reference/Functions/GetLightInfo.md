# GetLightInfo

## Description
Procedure GetLightInfo returns the attributes of the referenced light object.

**Table - Light Types**

| Light Type   | Constant |
|--------------|----------|
| Directional  | 0        |
| Point        | 1        |
| Spot         | 2        |

```pascal
PROCEDURE GetLightInfo(
				h              : HANDLE;
				VAR lightType  : INTEGER;
				VAR brightness : INTEGER;
				VAR isOn       : BOOLEAN;
				VAR castShadow : BOOLEAN);
```

```python
def vs.GetLightInfo(h):
    return (lightType, brightness, isOn, castShadow)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|lightType|INTEGER|Returns light type.|
|brightness|INTEGER|Returns light brightness.|
|isOn|BOOLEAN|Returns on-off status of light.|
|castShadow|BOOLEAN|Returns whether light casts shadows.|

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
