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

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
