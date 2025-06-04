# NurbsCurveEvalPt

## Description
This procedure determines the point on the nurbs curve at the given u value in the indexed piece.

The index is zero based (0 to number of knots - 1). The u value can range from 0 to the value of the last knot in the curve segment.

```pascal
PROCEDURE NurbsCurveEvalPt(
				objectHd     : HANDLE;
				index        : LONGINT;
				u            : REAL;
				VAR pX,pY,pZ : REAL);
```

```python
def vs.NurbsCurveEvalPt(objectHd, index, u):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to a NURBS curve.|
|index|LONGINT|Segment of curve to be queried.|
|u|REAL|Parameter between the minimum and maximum knot value.|
|p|REAL|Location of the u point on the curve.|

## See Also
VS Functions:
[NurbsKnot](NurbsKnot.md) 
| [NurbsNumKnots](NurbsNumKnots.md)

## Version
Availability: from VectorWorks9.5

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
