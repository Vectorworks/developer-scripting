# RegularPolygon

## Description
Creates an n-sided polygon.

```pascal
PROCEDURE RegularPolygon(
				centerX  : REAL;
				centerY  : REAL;
				radius   : REAL;
				numSides : INTEGER;
				mode     : INTEGER);
```

```python
def vs.RegularPolygon(centerX, centerY, radius, numSides, mode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|centerX|REAL|   |
|centerY|REAL|   |
|radius|REAL|   |
|numSides|INTEGER|   |
|mode|INTEGER|1 - circumscribed; 2 - inscribed|

## Examples
```pascal
RegularPolygon(1.0, 2.0, 0.5, 1, 2);
```
```python
import vs

# Creates an n-sided polygon.
centerX = 1.0
centerY = 2.0
radius = 1.0
numSides = 5
mode = 0

vs.RegularPolygon(centerX, centerY, radius, numSides, mode)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
