# Norm

## Description
Returns the length, or magnitude, of the specified vector.

```pascal
FUNCTION Norm(Vec : VECTOR): REAL;
```

```python
def vs.Norm(Vec):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Vec|VECTOR|Vector to be measured.|

## Remarks
(*_c_*, 2022.01.20) In Python the vector used as parameter MUST be 3-dimensional, or it will return gibberish. This doesn't matter in Pascal.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    vec :VECTOR;
BEGIN
    vec.x := 1;
    vec.y := 1.732050807;
    Message(Norm(vec));
END;
RUN(Example);

PROCEDURE Example2;
VAR
    v1, v2 : VECTOR;
BEGIN
    v1.x := 12; v1.y := 1;
    v2.x := 3; v2.y := 15;
    Message( Norm(v1-v2) );
END;
Run(Example2);
```
#### Python ####
```python
v1 = (12, 1, 0) # 3-dimensional tuple
v2 = (3, 15, 0)
vs.Message( str(vs.Norm( (v1[0] - v2[0], v1[1] - v2[1], v1[2] - v2[2]) )) )
```

## See Also
VS Functions:
[Distance](Distance.md)

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
