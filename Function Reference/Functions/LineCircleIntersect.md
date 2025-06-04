# LineCircleIntersect

## Description
Finds the intersection points of a line and a circle.

```pascal
FUNCTION LineCircleIntersect(
				begPt   : VECTOR;
				endPt   : VECTOR;
				cenPt   : VECTOR;
				radius  : REAL;
				VAR pt1 : VECTOR;
				VAR pt2 : VECTOR): BOOLEAN;
```

```python
def vs.LineCircleIntersect(begPt, endPt, cenPt, radius):
    return (BOOLEAN, pt1, pt2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|begPt|VECTOR|   |
|endPt|VECTOR|   |
|cenPt|VECTOR|   |
|radius|REAL|   |
|pt1|VECTOR|   |
|pt2|VECTOR|   |

## Remarks
In VS Python, this function returns 3-element tuples with gibberish in the third element regardless whether you give it 2- or 3-element tuples.
This function checks and returns the intersection of the circle with an infinite line defined by the two supplied points.

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
