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

## Examples
```pascal
{* Get the location of the centroid *}
OK := Centroid3D (gObjH, gXc, gYc, gZc);

BEGIN
	OK := Centroid3D (gObjH, gXc, gYc, gZc);
	OK := Moments3D (gObjH, gIxx, gIyy, gIzz);
	IF gIxx > 0 THEN gKx := Sqrt (gIxx) ELSE gKx := 0;
	IF gIyy > 0 THEN gKy := Sqrt (gIyy) ELSE gKy := 0;
	IF gIzz > 0 THEN gKz := Sqrt (gIzz) ELSE gKz := 0;
```
```python
import vs

# Returns the center of gravity of a 3D object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, xCG, yCG, zCG = vs.Centroid3D(obj)
vs.Message('Centroid3D returned: ' + str((ok, xCG, yCG, zCG)))
```

## Version
Availability: from VectorWorks 10.1

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
