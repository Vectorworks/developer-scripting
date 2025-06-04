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

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
