# PointAlongPolyN

## Description
Returns a point at the specified distance along the poly, and a vector tangent to the poly at that point. Similar to PointAlongPoly with an addition of an epsilon value.

```pascal
FUNCTION PointAlongPolyN(
				h           : HANDLE;
				dist        : REAL;
				epsilon     : REAL;
				VAR pt      : VECTOR;
				VAR tangent : VECTOR): BOOLEAN;
```

```python
def vs.PointAlongPolyN(h, dist, epsilon):
    return (BOOLEAN, pt, tangent)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|dist|REAL|   |
|epsilon|REAL|   |
|pt|VECTOR|   |
|tangent|VECTOR|   |

## See Also
VS Functions:
* [PointAlongPoly](PointAlongPoly.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
