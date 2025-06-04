# OverlapLineLine

## Description
Returns two points the lap zone of two lines.

```pascal
FUNCTION OverlapLineLine(
				begPt1     : VECTOR;
				endPt1     : VECTOR;
				begPt2     : VECTOR;
				endPt2     : VECTOR;
				VAR lapPt1 : VECTOR;
				VAR lapPt2 : VECTOR;
				tolerance  : REAL): BOOLEAN;
```

```python
def vs.OverlapLineLine(begPt1, endPt1, begPt2, endPt2, tolerance):
    return (BOOLEAN, lapPt1, lapPt2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|begPt1|VECTOR|   |
|endPt1|VECTOR|   |
|begPt2|VECTOR|   |
|endPt2|VECTOR|   |
|lapPt1|VECTOR|   |
|lapPt2|VECTOR|   |
|tolerance|REAL|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
