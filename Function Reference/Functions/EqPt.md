# EqPt

## Description
Returns TRUE if the 2D points are equal within the tolerance.

```pascal
FUNCTION EqPt(
				pt1       : VECTOR;
				pt2       : VECTOR;
				tolerance : REAL): BOOLEAN;
```

```python
def vs.EqPt(pt1, pt2, tolerance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt1|VECTOR|   |
|pt2|VECTOR|   |
|tolerance|REAL|   |

## Remarks
([[User:CBM-c-|_c_]], 2022.01.21) Tolerance must be <> 0. By a tolerance of 0 EqPt will always return false. In Python, contrary to most Pascal-derived vectorial routines, EqPt accepts also a bidimensional tuple without returning gibberish: the third item will always be ignored. So this is a 2D-only routine.

## Examples
==== Vectorscript ====
```pascal
PROCEDURE Example;
VAR
    v1, v2 : VECTOR;
BEGIN
    v1.x := 12; v1.y := 1;
    v2.x := 12; v2.y := 1;
    Message(Concat( EqPt(v1, v2, 0.1) ));
END;
Run(Example);
```
==== Python ====
```python
v1 = (12, 1, 999) # z vals in 3-dimensional tuples will be ignored
v2 = (12, 1, 0)
vs.Message( str(vs.EqPt(v1, v2, 0.1)) )
```

## See Also
VS Functions:
* [EqualPt](EqualPt.md)
* [EqPt2D](EqPt2D.md)
* [EqPt3D](EqPt3D.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
