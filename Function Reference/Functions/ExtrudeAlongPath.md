# ExtrudeAlongPath

## Description
Creates a new path extrude object in the document.  The profile defines the shape of the cross-section, and is extruded along the path to generate the resulting object.<BR>
<BR>
The path argument must be a handle to a NURBS Curve object (type 111).  The profile argument must be a handle to an object of one of the following types: NURBS Curve, Polygon, Polyline, Arc, Rectangle, Rounded Rectangle, Line, Oval.<BR>

```pascal
FUNCTION ExtrudeAlongPath(
				pathHandle    : HANDLE;
				profileHandle : HANDLE): HANDLE;
```

```python
def vs.ExtrudeAlongPath(pathHandle, profileHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pathHandle|HANDLE|Handle to the path object.|
|profileHandle|HANDLE|Handle to the profile object.|

## Remarks
*\_c\_*, 2018.05.13: The generated extrusion is a Generic Solid and won't take the active class attributes, while CreateExtrudeAlongPath will create a number of NURBS curves with class attributes, but they won't section properly in Section Viewports without stitch and trim, since they don't generate a fill. Tested in Pio: OK.


-----
The generic solid can not be edited

The following objects are supported as profile objects:

* 2	-	Line
* 3	-	Box
* 4	-	Oval
* 5	-	Polygon
* 6	-	Arc
* 8	-	Freehand
* 13 -	R Rect
* 21 -	Polyline
* 25 -	3D Poly
* 111 -	NURBS Curve

## See Also
VS Functions:
[CreateExtrudeAlongPath](CreateExtrudeAlongPath.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
