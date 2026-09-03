# Ang2Vec

## Description
Returns a 3-dimensional vector that is defined by the specified polar angle and length values.

```pascal
FUNCTION Ang2Vec(
				angleR : REAL;
				Length : REAL): VECTOR;
```

```python
def vs.Ang2Vec(angleR, Length):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|angleR|REAL|The angle of the vector (in degrees).|
|Length|REAL|The length of the vector.|

## Remarks
(*\_c\_*, 2022.01.20) The vector returned is always 3-dimensional whereby the last item is always 0: Pascal: {x, y, z}, Python: tuple (0.0, 0.0, 0.0)

## Examples
#### VectorScript ####
```python
Message( Ang2Vec(45, 1) ); { 3-dimensional vector whose z item is always 0 }
```
#### Python ####
```python
v = vs.Ang2Vec(45, 1)
vs.Message( str( v ) ) # 3-dimensional tuple whose last item is always 0
```

```pascal
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

polyPt [1] := u [1] + Ang2Vec (-theta4, j*s1);

BEGIN
temp_b := PointAlongPoly(basepoly_h,(temp_i*spacing),pt,tangent);
basepoints[temp_i] := pt;
tmp1_v := tangent;
tmp1_v := ang2vec(vec2ang(tmp1_v)+90,-corru_ht);
ctrpoints[temp_i] := basepoints[temp_i] + tmp1_v;
END;
```
```python
	theta1 = theta1 + theta2
v1.x = x0
v1.y = y0
v	= Vector(vs.Ang2Vec( theta1, r ))
v2 = v1 + v
vs.Absolute()
if drawing3D:
	vs.Add3DPt( v2.x, v2.y, z )
```
See also in tutorials: [11. 2D Vector Math Toolkit](ai%20examples/11_VectorMathToolkit.md)

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
