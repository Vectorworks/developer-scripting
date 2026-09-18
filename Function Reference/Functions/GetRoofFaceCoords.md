# GetRoofFaceCoords

## Description
Returns the coordinates of the defining geometry of a roof face.

```pascal
PROCEDURE GetRoofFaceCoords(
				h                     : HANDLE;
				VAR axis1X,axis1Y     : REAL;
				VAR axis2X,axis2Y     : REAL;
				VAR Zaxis             : REAL;
				VAR upslopeX,upslopeY : REAL);
```

```python
def vs.GetRoofFaceCoords(h):
    return (axis1, axis2, Zaxis, upslope)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to roof face object.|
|axis1|REAL|X-Y coordinates of first axis point.|
|axis2|REAL|X-Y coordinates of second axis point.|
|Zaxis|REAL|Elevation of roof axis.|
|upslope|REAL|X-Y coordinates of roof upslope point.|

## Remarks
Returns information about old-style roof objects (single roof faces).

Returns roof definition axis, upslope definition point.

See Also GetRoofFaceAttr() for additional roof face data

## Examples
[GetRoofProperties](examples/GetRoofProperties.md)

```pascal
GetRoofFaceCoords(h, 1.0, 2.0, 0.5, 1.5, 3.0, 1.0, 2.0);
```
```python
import vs

# Returns the coordinates of the defining geometry of a roof face.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

axis1, axis2, Zaxis, upslope = vs.GetRoofFaceCoords(h)
vs.Message('GetRoofFaceCoords returned: ' + str((axis1, axis2, Zaxis, upslope)))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
