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
#### VectorScript ####
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
#### Python ####
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

```pascal
bUseGroup := FALSE;
HANDLE_cnt := 0;
IF layers[cnt].sel THEN BEGIN
	{Create the slice.}
	curve_h := CreateContourCurves(solid_h, 0, 0, 0, layers[cnt].base, 0, 0, 1);
	if (curve_h <> NIL) & ((GetType(curve_h) = 111) | (GetType(curve_h) = 11)) then BEGIN
		{Now change the Layer to that of the target Layer.}
		b := SetParent(curve_h, GetLayerByName(layers[cnt].name));
			if drawWalls_b | leaveFrame then BEGIN
```
```python
import vs

# Creates contour curves for a solid object given the delta, point on plane
# and plane normal.
inSourceObject = vs.FSActLayer()  # handle to the first selected object on the active layer
delta = 1.0
ptOnPlane = 'Example'
normal = 'Example'

objHandle = vs.CreateContourCurves(inSourceObject, delta, ptOnPlane, normal)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
