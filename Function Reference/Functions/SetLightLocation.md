# SetLightLocation

## Description
Procedure SetLightLocation sets the location of the referenced light object.

```pascal
PROCEDURE SetLightLocation(
				h      : HANDLE;
				pX,pY  : REAL;
				zValue : REAL);
```

```python
def vs.SetLightLocation(h, p, zValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|p|REAL|X-Y coordinate location of light.|
|zValue|REAL|Elevation of light.|

## Examples
```pascal
BEGIN
SetLightLocation(CurLightHandle, CurLightXLoc, CurLightYLoc, CurLightZLoc);
END;

BEGIN
SetLightLocation(LightObjHandle,
				gLightXLoc[SceneNumber, LightNumber],
				gLightYLoc[SceneNumber, LightNumber],
				gLightZLoc[SceneNumber, LightNumber]
				);
END;
```
```python
import vs

# Procedure SetLightLocation sets the location of the referenced light object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
p = (0, 0)
zValue = 0.0

vs.SetLightLocation(h, p, zValue)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
