# GetLightDirection

## Description
Procedure GetLightDirection returns the direction angles of the referenced light object.

```pascal
PROCEDURE GetLightDirection(
				h              : HANDLE;
				VAR panAngleR  : REAL;
				VAR tiltAngleR : REAL);
```

```python
def vs.GetLightDirection(h):
    return (panAngleR, tiltAngleR)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|panAngleR|REAL|Returns light pan angle.|
|tiltAngleR|REAL|Returns light tilt angle.|

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
