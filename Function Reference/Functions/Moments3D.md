# Moments3D

## Description
Returns the moments of inertia of a 3D object about the x, y, and z axes of a point at the center of gravity of the object.

```pascal
FUNCTION Moments3D(
				obj     : HANDLE;
				VAR lxx : REAL;
				VAR lyy : REAL;
				VAR lzz : REAL): BOOLEAN;
```

```python
def vs.Moments3D(obj):
    return (BOOLEAN, lxx, lyy, lzz)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object for which to find the 3D moments.|
|lxx|REAL|The moment of inertia relative to the x-axis passing through the center of mass of object|
|lyy|REAL|The moment of inertia relative to the y-axis passing through the center of mass of object|
|lzz|REAL|The moment of inertia relative to the z-axis passing through the center of mass of object|

## Version
Availability: from VectorWorks 10.1

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
