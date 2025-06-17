# EqPt2D

## Description
Returns TRUE if the 2D points are equal within the tolerance

```pascal
FUNCTION EqPt2D(
				pt1       : VECTOR;
				pt2       : VECTOR;
				tolerance : REAL): BOOLEAN;
```

```python
def vs.EqPt2D(pt1, pt2, tolerance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt1|VECTOR|   |
|pt2|VECTOR|   |
|tolerance|REAL|   |

## Remarks
(*\_c\_*, 2022.01.21) :
* Python: contrary to most Pascal-derived vectorial routines, it accepts also a bidimensional tuple without returning gibberish: the third item will always be ignored. 
* Python and Pascal: Don't pass 0 to the tolerance, or the routine will always return false.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    v1, v2 : VECTOR;
BEGIN
    v1.x := 12; v1.y := 1; 
    v2.x := 12; v2.y := 1;
    Message(Concat( EqPt2D(v1, v2, 0.1) )); {True }
END;
Run(Example);
```
#### Python ####
```python
v1 = (12, 1, 987) # 3-dimensional tuples: the 3rd item will be ignored
v2 = (12, 1, 0)
vs.Message( str(vs.EqPt2D(v1, v2, 0.1)) ) # True
```

## See Also
VS Functions:
* [EqualPt](EqualPt.md)
* [EqPt](EqPt.md)
* [EqPt3D](EqPt3D.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
