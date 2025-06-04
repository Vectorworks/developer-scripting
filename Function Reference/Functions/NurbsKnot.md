# NurbsKnot

## Description
Returns the specified knot in a NURBS curve or surface.

For NURBS curves, index1 corresponds to the segment of the curve to be queried, and index2 corresponds to the knot in the segment.

For NURBS surfaces, index1 corresponds to the u- or v-direction of the surface (u=1, v=0), and index2 corresponds to the knot index. 

The index is zero based (0 to number of knots - 1).

```pascal
PROCEDURE NurbsKnot(
				objectHd : HANDLE;
				index1   : LONGINT;
				index2   : LONGINT;
				VAR knot : REAL);
```

```python
def vs.NurbsKnot(objectHd, index1, index2):
    return knot
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index1|LONGINT|Segment of curve to be queried (NURBS curve), or direction (NURBS surface).|
|index2|LONGINT|Index of segment or direction knot.|
|knot|REAL|Knot value.|

## Remarks
this function will work for both nurbs curves and nurbs surfaces

## Examples
==== VectorScript ====
```pascal
See NurbsSurfaceEvalPt
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
