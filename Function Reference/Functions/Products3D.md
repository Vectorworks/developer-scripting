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

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
