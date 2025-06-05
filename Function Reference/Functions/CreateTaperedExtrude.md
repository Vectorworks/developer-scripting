# CreateTaperedExtrude

## Description
Creates a new tapered extrude object in the document.

```pascal
FUNCTION CreateTaperedExtrude(
				profileH : HANDLE;
				angle    : REAL;
				height   : REAL): HANDLE;
```

```python
def vs.CreateTaperedExtrude(profileH, angle, height):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|profileH|HANDLE|Handle to object defining profile geometry.|
|angle|REAL|Taper angle of extrude (in degrees).|
|height|REAL|Height of extrude.|

## Remarks
*_c_*, (2016.02.10):  This always fails creating a number of NURBS instead of a tapered extrude. From VW 2016 you can use [[VS:CreateTaperedExtrd2]].

## Version
Availability: from VectorWorks 9.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
