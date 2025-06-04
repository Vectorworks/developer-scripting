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
tRoofProperties}}

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
