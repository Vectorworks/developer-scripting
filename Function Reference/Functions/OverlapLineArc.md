# OverlapLineArc

## Description
Finds the overlap of a line and an arc. Returns the overlapping segment if it exists.

```pascal
FUNCTION OverlapLineArc(
				begPt      : VECTOR;
				endpt      : VECTOR;
				cenPt      : VECTOR;
				radius     : REAL;
				startAng   : REAL;
				sweepAng   : REAL;
				VAR lapPt1 : VECTOR;
				VAR lapPt2 : VECTOR;
				tolerance  : REAL): BOOLEAN;
```

```python
def vs.OverlapLineArc(begPt, endpt, cenPt, radius, startAng, sweepAng, tolerance):
    return (BOOLEAN, lapPt1, lapPt2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|begPt|VECTOR|   |
|endpt|VECTOR|   |
|cenPt|VECTOR|   |
|radius|REAL|   |
|startAng|REAL|   |
|sweepAng|REAL|   |
|lapPt1|VECTOR|   |
|lapPt2|VECTOR|   |
|tolerance|REAL|   |

## Examples
```pascal
resultOK := OverlapLineArc(begPt, endpt, cenPt, 1.0, 2.0, 0.5, lapPt1, lapPt2, 1.5);
```
```python
import vs

# Finds the overlap of a line and an arc.
begPt = (0, 0)
endpt = (2, 2)
cenPt = (2, 0)
radius = 1.0
startAng = 1.0
sweepAng = 2.0
tolerance = 0.5

ok, lapPt1, lapPt2 = vs.OverlapLineArc(begPt, endpt, cenPt, radius, startAng, sweepAng, tolerance)
vs.Message('OverlapLineArc returned: ' + str((ok, lapPt1, lapPt2)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
