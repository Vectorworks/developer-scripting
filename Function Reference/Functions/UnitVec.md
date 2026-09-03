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

```pascal
GetUnits(fraction, display, format, upi, name, sqName);
halfFont := kHalfFont * upi * GetLScale(ActLayer);
tmpAngle := Vec2Ang(segVector);
tmpVector := 0.5*segVector;
labelVector := -1 * Perp(UnitVec(tmpVector)) * halfFont;

{determine the closer end of the text to the Group, as if text has a changed justification it is possible that}
{the origin might be on the further side of the text block or in its center!!!!}
{left justified text}
IF ( GetTextJust( textH ) = 1 ) THEN
	tempV := UnitVec( Ang2Vec( ang , 1) ) * GetTextWidth( textH ) + originVec
{right justified text}
ELSE IF ( GetTextJust( textH ) = 3 ) THEN tempV := UnitVec( Ang2Vec( ang + 180 , 1) ) * GetTextWidth( textH ) + originVec
{center justified text}
else BEGIN
	tempV := UnitVec( Ang2Vec( ang , 1) ) * GetTextWidth( textH )/2 + originVec;
	originVec := UnitVec( Ang2Vec( ang + 180 , 1) ) * GetTextWidth( textH )/2 + originVec;
END;

BEGIN
	u1 := v [3] - v [1];
	u1 := v [1] + Norm (u1) * UnitVec (u1) / 2;
```
```python
import vs

# Returns the standard unit vector of the specified vector.
Vect = (0, 0)

vec = vs.UnitVec(Vect)
vs.Message('UnitVec returned: ' + str(vec))
```

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
