# CreateContourCurves

## Description
Creates contour curves for  a solid object given the delta, point on plane and plane normal.  If delta is 0, only 1 curve is created, where the specified plane intersects the selected solid.

```pascal
FUNCTION CreateContourCurves(
				inSourceObject                   : HANDLE;
				delta                            : REAL;
				ptOnPlaneX,ptOnPlaneY,ptOnPlaneZ : REAL;
				normalX,normalY,normalZ          : REAL): HANDLE;
```

```python
def vs.CreateContourCurves(inSourceObject, delta, ptOnPlane, normal):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inSourceObject|HANDLE|Handle to a solid object|
|delta|REAL|Distance between contours|
|ptOnPlane|REAL|Point on plane used to define contours|
|normal|REAL|Plane's normal vector|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
inSourceObject :HANDLE; 
delta :REAL; 
ptOnPlaneX, ptOnPlaneY, ptOnPlaneZ :REAL; 
normalX, normalY, normalZ :REAL;
h :HANDLE;
BEGIN
inSourceObject := FSActLayer;
delta := 0; {number of slices}
ptOnPlaneX := 0;
ptOnPlaneY := 0;
ptOnPlaneZ := 610;
normalX := 0;
normalY := 0;
normalZ := 1;
h := CreateContourCurves(inSourceObject, delta, ptOnPlaneX, ptOnPlaneY, ptOnPlaneZ, normalX, normalY, normalZ);
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	inSourceObject = vs.FSActLayer()
	delta = 0 #{number of slices}
	ptOnPlaneX = 0
	ptOnPlaneY = 0
	ptOnPlaneZ = 610
	normalX = 0
	normalY = 0
	normalZ = 1
	h = vs.CreateContourCurves(inSourceObject, delta, ptOnPlaneX, ptOnPlaneY, ptOnPlaneZ, normalX, normalY, normalZ)
Example()
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
