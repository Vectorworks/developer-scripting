# Products3D

## Description
Returns the products of inertia of a 3D object for the xy, yz, and zx planes passing through a point at the center of gravity of the object.

```pascal
FUNCTION Products3D(
				obj     : HANDLE;
				VAR lxy : REAL;
				VAR lyz : REAL;
				VAR lzx : REAL): BOOLEAN;
```

```python
def vs.Products3D(obj):
    return (BOOLEAN, lxy, lyz, lzx)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object from which to calculate the Products|
|lxy|REAL|Theh product of inertia with respect to the YZ and XZ planes passing through the center of mass of object.|
|lyz|REAL|Theh product of inertia with respect to the XZ and XY planes passing through the center of mass of object.|
|lzx|REAL|Theh product of inertia with respect to the XY and YZ planes passing through the center of mass of object.|

## Examples
```pascal
OK := Moments3D (gObjH, gIxx, gIyy, gIzz);
IF gIxx > 0 THEN gKx := Sqrt (gIxx) ELSE gKx := 0;
IF gIyy > 0 THEN gKy := Sqrt (gIyy) ELSE gKy := 0;
IF gIzz > 0 THEN gKz := Sqrt (gIzz) ELSE gKz := 0;
OK := Products3D (gObjH, gIxy, gIyz, gIzx);
gIsSolid := (gIxx > 0) & (gIyy > 0) & (gIzz > 0);
```
```python
import vs

# Returns the products of inertia of a 3D object for the xy, yz, and zx
# planes passing through a point at the center of gravity of the object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, lxy, lyz, lzx = vs.Products3D(obj)
vs.Message('Products3D returned: ' + str((ok, lxy, lyz, lzx)))
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
