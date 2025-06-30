# CreateExtrudeAlongPath

## Description
Creates a new path extrude object in the document.  The profile defines the shape of the cross-section, and is extruded along the path to generate the resulting object.

The path argument must be a handle to a NURBS Curve object (type 111).  The profile argument must be a handle to an object of one of the following types: NURBS Curve, Polygon, Polyline, Arc, Rectangle, Rounded Rectangle, Line, Oval.

```pascal
FUNCTION CreateExtrudeAlongPath(
				pathHandle    : HANDLE;
				profileHandle : HANDLE): HANDLE;
```

```python
def vs.CreateExtrudeAlongPath(pathHandle, profileHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pathHandle|HANDLE|Handle to the path object.|
|profileHandle|HANDLE|Handle to the profile object.|

## Remarks
*\_c\_*, 2018.05.13: It creates a number of NURBS curves with class attributes, these won't section properly in Section Viewports without stitch and trim since they don't have a fill. Tested in Pio: OK. [ExtrudeAlongPath](ExtrudeAlongPath.md) outputs generic solids instead, but it won't take up the active class attributes.

Older remarks not from me (\_c\_):

The following objects are supported as profile objects:

|Object Type|Type Number|
|---|---|
|Line|2|
|Box|3|
|Oval|4|
|Polygon|5|
|Arc|6|
|Freehand|8|
|R Rect|13|
|Polyline|21|
|3D Poly|25|
|NURBS Curve|111|


This works from inside a VSO, but I couldn't get it to work using an oval. I was able to get it to work with an arc.



This will fail if the NURBS curve has two consecutive segments which are colinear, or nearly colinear. In the example that I tested, the failure occured if the segments were colinear within .375 degree, but I don't know if the failure criterion is the angular difference or a combination of other factors (length, width of profile, shape of profile, etc.).


In VW2011 this will generate a number of NURBS surfaces instead of an extrude along path object.

## Version
Availability: from VectorWorks 9.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
