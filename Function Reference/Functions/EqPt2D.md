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

```pascal
IF( ( NOT EqPt2D( vec1, vec, .0000000001 ) ) & ( NOT EqPt2D( vec2, vec, .0000000001  ) ) ) THEN
BEGIN
	hForDel := tempH;
	tempH := NextObj( tempH );
	DelObject( hForDel );
END ELSE
BEGIN

BEGIN
	IF not (EqPt2D(pt1, pt2, fuzz)) THEN BEGIN
		ndx1 := AddUniquePts(pt1);
		ndx2 := AddUniquePts(pt2);
		lineCnt := lineCnt + 1;
		lines[lineCnt].p1 := ndx1;
		lines[lineCnt].p2 := ndx2;

{//// if the location of the viewport is the same before and after the second layer is made visible, vpRespectsDLayZHtFunc is TRUE, else FALSE }
vpRespectsDLayZHtFunc := EqPt2D( testPt_1, testPt_2, 0.00000001 );
```
```python
import vs

# Returns TRUE if the 2D points are equal within the tolerance.
pt1 = (0, 0)
pt2 = (1, 1)
tolerance = 1.0

ok = vs.EqPt2D(pt1, pt2, tolerance)
if ok:
    vs.Message('EqPt2D succeeded')
else:
    vs.Message('EqPt2D failed')
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
