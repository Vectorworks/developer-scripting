# Centroid3D

## Description
Returns the center of gravity of a 3D object. The function returns TRUE if the values were found.

```pascal
FUNCTION Centroid3D(
				obj     : HANDLE;
				VAR xCG : REAL;
				VAR yCG : REAL;
				VAR zCG : REAL): BOOLEAN;
```

```python
def vs.Centroid3D(obj):
    return (BOOLEAN, xCG, yCG, zCG)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The objectt from whci to calculate the center of gravity|
|xCG|REAL|The x component of the center of gravity.|
|yCG|REAL|The y component of the center of gravity.|
|zCG|REAL|The z component of the center of gravity.|

## Version
Availability: from VectorWorks 10.1

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
