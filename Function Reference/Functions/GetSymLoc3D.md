# GetSymLoc3D

## Description
Determines the location of a specified symbol or plug-in object in 3D space.

```pascal
PROCEDURE GetSymLoc3D(
				objectHandle : HANDLE;
				VAR x        : REAL;
				VAR y        : REAL;
				VAR z        : REAL);
```

```python
def vs.GetSymLoc3D(objectHandle):
    return (x, y, z)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to a symbol instance or a plug-in object in the drawing.|
|x|REAL|The location of the object along the x-axis.|
|y|REAL|The location of the object along the y-axis.|
|z|REAL|The location of the object along the z-axis.|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
