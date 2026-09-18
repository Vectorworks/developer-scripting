# SrndArea

## Description
Function SrndArea when given a point, returns the area of the smallest polygon bounded by the selected objects.

```pascal
FUNCTION SrndArea(pX,pY : REAL): REAL;
```

```python
def vs.SrndArea(p):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinates of reference point.|

## Remarks
Given a point, returns the area of the smallest polygon bounded by the selected objects.  Returns nil if none can be found. 

[sd 8/18/98]

## Examples
```pascal
resultVal := SrndArea(1.0, 2.0);
```
```python
import vs

# Function SrndArea when given a point, returns the area of the smallest
# polygon bounded by the selected objects.
p = (0, 0)

area = vs.SrndArea(p)
vs.Message('SrndArea returned: ' + str(area))
```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
