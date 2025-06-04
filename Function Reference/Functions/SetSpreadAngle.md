# SetSpreadAngle

## Description
Procedure SetSpreadAngle sets the spread angle of the light object. If the light type is not a spot light, the procedure has no effect on the light.

```pascal
PROCEDURE SetSpreadAngle(
				h            : HANDLE;
				spreadAngleR : REAL);
```

```python
def vs.SetSpreadAngle(h, spreadAngleR):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|spreadAngleR|REAL|Beam spread angle of light.|

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
