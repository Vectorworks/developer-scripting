# Poly

## Description
Procedure Poly creates a polygon object in the document. Vertices of the polygon are specified by a parameter list of x1,y1 through xn,yn, which correspond to the coordinate locations of each vertex.

```pascal
PROCEDURE Poly(p : REAL);
```

```python
def vs.Poly(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|   |

## Examples
#### VectorScript ####
```pascal
Poly(0,0,-0.5,1,0.5,1.5,2,1,1,-0.5);
```
#### Python ####
```python
vs.Poly(0,0,-0.5,1,0.5,1.5,2,1,1,-0.5)

# Or using a list:
points = [0,0,-0.5,1,0.5,1.5,2,1,1,-0.5]
vs.Poly(*points)
```

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
