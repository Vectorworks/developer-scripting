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

## Examples
```pascal
					)
			);
}
WHILE	(
		PointAlongPolyN( HighlightClonePoly, HighlightDashDist, 0, HighlightDashPt_1, HighlightDashTangPt )
		AND
		PointAlongPolyN( HighlightClonePoly, HighlightDashDist + HighlightDashIncr, 0, HighlightDashPt_2, HighlightDashTangPt )
		)
DO	BEGIN
		{
		AlrtDialog( Concat( 'HighlightDashDist: ', HighlightDashDist ) );
		}

BEGIN
	IF PointAlongPolyN(GetCustomObjectPath(ghParm),gOpenWidth,0,SegStart,TestTanVec) THEN BEGIN END;
	IF PointAlongPolyN(GetCustomObjectPath(ghParm),(Length-gOpenWidth)/2+gOpenWidth,0,SegMid,TestTanVec) THEN BEGIN END;

IF PointAlongPolyN(hLocPath,rLocDistance,0,MidVec,TestTanVec) THEN BEGIN END;
IF PointAlongPolyN(hLocPath,rLocDistance+kMeasInc,0,PosVec,TestTanVec) THEN BEGIN END;
IF PointAlongPolyN(hLocPath,rLocDistance-kMeasInc,0,NegVec,TestTanVec) THEN BEGIN END;
```
```python
import vs

# Returns a point at the specified distance along the poly, and a vector
# tangent to the poly at that point.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
dist = 1.0
epsilon = 1.0

ok, pt, tangent = vs.PointAlongPolyN(h, dist, epsilon)
vs.Message('PointAlongPolyN returned: ' + str((ok, pt, tangent)))
```

## See Also
VS Functions:
* [PointAlongPoly](PointAlongPoly.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
