# WallPeak

## Description
Creates a wall peak of the specified height at a specified distance from the wall start point.

There is no error checking of the distance or peak height parameters; it is left to the programmer to ensure that the parameter values are valid.

```pascal
PROCEDURE WallPeak(
				alongDistance  : REAL;
				heightDistance : REAL);
```

```python
def vs.WallPeak(alongDistance, heightDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|alongDistance|REAL|Location of peak (measured from wall start point).|
|heightDistance|REAL|Elevation of wall peak.|

## Examples
==== VectorScript ====
```pascal
SetZVal(0',8');
Wall(0,0,7,0);
WallPeak(3'-6&quot;,9'-0&quot;);
{creates a 9' wall peak 3'-6&quot; from the start point of the wall}
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
