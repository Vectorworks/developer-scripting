# Poly3D

## Description
Procedure Poly3D creates a three dimensional polygon in a VectorWorks document. The vertices of the polygon are specified by a list of parameters x1, y1, z1 through xn, yn, and zn, which specify the coordinate locations of each vertex.

```pascal
PROCEDURE Poly3D(p : REAL);
```

```python
def vs.Poly3D(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|   |

## Examples
==== VectorScript ====
```pascal
Poly3D(1,1,0,1.5,1.5,1,2.5,1.5,1,);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
