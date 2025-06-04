# Distance

## Description
Function Distance returns the distance between the two specified coordinate locations.

```pascal
FUNCTION Distance(
				x1 : REAL;
				y1 : REAL;
				x2 : REAL;
				y2 : REAL): REAL;
```

```python
def vs.Distance(x1, y1, x2, y2):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x1|REAL|X coordinate of first point.|
|y1|REAL|Y coordinate of first point.|
|x2|REAL|X coordinate of second point.|
|y2|REAL|Y coordinate of second point.|

## Examples
==== VectorScript ====
```pascal
d:=Distance(0,2,4,5);
{returns the distance between (0,2) and (4,5)}
```
==== Python ====
```python
d= vs.Distance(0,2,4,5)
```

## See Also
VS Functions:
[Norm](Norm.md)

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
