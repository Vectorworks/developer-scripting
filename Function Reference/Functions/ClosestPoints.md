# ClosestPoints

## Description
Returns the points on two objects where the shortest distance between those objects occurs. Should support all VW primitives, including polylines and NURBS. Would be nice if it supported groups, symbols, and PIOs. Would also be nice if it supported 3D.

```pascal
PROCEDURE ClosestPoints(
				h1           : HANDLE;
				h2           : HANDLE;
				VAR pt1      : VECTOR;
				VAR pt2      : VECTOR;
				VAR touching : BOOLEAN);
```

```python
def vs.ClosestPoints(h1, h2):
    return (pt1, pt2, touching)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h1|HANDLE|   |
|h2|HANDLE|   |
|pt1|VECTOR|   |
|pt2|VECTOR|   |
|touching|BOOLEAN|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
