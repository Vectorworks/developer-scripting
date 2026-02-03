# UnitVec

## Description
Returns the standard unit vector of the specified vector.

```pascal
FUNCTION UnitVec(Vect : VECTOR): VECTOR;
```

```python
def vs.UnitVec(Vect):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Vect|VECTOR|Source vector.|

## Remarks
(\_c\_, 2022.01.19) The vector returned is always 3-dimensional: Pascal: vector {x, y, z}, Python: tuple (0.0, 0.0, 0.0).
Note: in Python the vector used as parameter MUST be 3-dimensional, or UnitVec will return gibberish. This doesn't matter in Pascal.

## Examples
#### VectorScript ####
```pascal
PROCEDURE TEST;
VAR
    v1, v2 : VECTOR;

BEGIN
    v1.x := 12; v1.y := 1; v1.z := 0; { can be a 3-dimensional Vector, doesn't need to, though }
    v2.x := 3; v2.y := 15; v2.z := 0;
    Message( UnitVec(v1 - v2)); { returns a 3-dimensional Vector }
END;
Run(TEST);
```
#### Python ####
```python
v1 = (12, 1, 0) # must be a 3-dimensional tuple, or you'll get gibberish in the returned vector
v2 = (3, 15, 0)
vs.Message( str(vs.UnitVec( (v1[0] - v2[0], v1[1] - v2[1], v1[2] - v2[2]) )) ) # returns a 3-dimensional tuple
```

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
