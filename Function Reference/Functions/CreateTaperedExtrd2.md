# CreateTaperedExtrd2

## Description
Creates a new tapered extrude object in the document. This function returns a "general solid" object while the other function, [CreateTaperedExtrude](CreateTaperedExtrude.md), produces a bunch of NURBS surfaces.

```pascal
FUNCTION CreateTaperedExtrd2(
				profileH : HANDLE;
				angle    : REAL;
				height   : REAL): HANDLE;
```

```python
def vs.CreateTaperedExtrd2(profileH, angle, height):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|profileH|HANDLE|Handle to object defining profile geometry.|
|angle|REAL|Taper angle of extrude (in degrees).|
|height|REAL|Height of extrude.|

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
