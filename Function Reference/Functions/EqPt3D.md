# EqPt3D

## Description
Returns TRUE if the 3D points are equal within the tolerance.

```pascal
FUNCTION EqPt3D(
				pt1       : VECTOR;
				pt2       : VECTOR;
				tolerance : REAL): BOOLEAN;
```

```python
def vs.EqPt3D(pt1, pt2, tolerance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt1|VECTOR|   |
|pt2|VECTOR|   |
|tolerance|REAL|   |

## Remarks
(_c_, 2022.01.22) :
* Python: contrary to most Pascal-derived vectorial routines, it accepts also bidimensional tuples or even a 2/3-dimensional mix
* Python and Pascal: Don't pass 0 to the tolerance, or the routine will always return false.

## Examples
==== Vectorscript ====
```pascal
PROCEDURE Example;
VAR
    v1, v2 : VECTOR;
BEGIN
    v1.x := 12; v1.y := 1; v1.z := 999;
    v2.x := 12; v2.y := 1; v2.z := 999.01;

    Message(Concat( EqPt3D(v1, v2, 0.1) )); { returns true }
    Message(Concat( EqPt3D(v1, v2, 0.01) )); { returns false }
    Message(Concat( EqPt3D(v1, v2, 0) )); { always returns false! Don't use tolerance zero }
END;
Run(Example);
```
==== Python ====
```python
v1 = (12, 1, 999) # also accepts bidimensional tuples
v2 = (12, 1, 999)
vs.Message( str(vs.EqPt3D(v1, v2, 0.01)) ) # returns true

# example with faulty tolerance
v1 = (12, 1, 999)
v2 = (12, 1, 999)
vs.Message( str(vs.EqPt3D(v1, v2, 0)) ) # always returns false! Don't use tolerance zero
```

## See Also
VS Functions:
* [EqualPt](EqualPt.md)
* [EqPt](EqPt.md)
* [EqPt2D](EqPt2D.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
