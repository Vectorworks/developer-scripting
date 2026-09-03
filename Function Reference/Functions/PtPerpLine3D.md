# PtPerpLine3D

## Description
Returns a 3D point on the input 3D vector that goes through pt0 and pt1 which is closest to the input point. Doesn't check to see that the point is ON the line.

```pascal
FUNCTION PtPerpLine3D(
				pt  : VECTOR;
				pt0 : VECTOR;
				pt1 : VECTOR) : VECTOR;
```

```python
def vs.PtPerpLine3D(pt, pt0, pt1):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt|VECTOR||
|pt0|VECTOR||
|pt1|VECTOR||

## Examples
```pascal
result := PtPerpLine3D(pt, pt0, pt1);
```
```python
import vs

# Returns a 3D point on the input 3D vector that goes through pt0 and pt1
# which is closest to the input point.
pt = (0, 0)
pt0 = (1, 1)
pt1 = (2, 2)

vec = vs.PtPerpLine3D(pt, pt0, pt1)
vs.Message('PtPerpLine3D returned: ' + str(vec))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
