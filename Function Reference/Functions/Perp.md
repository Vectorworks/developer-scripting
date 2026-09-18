# Perp

## Description
Returns a vector which is perpendicular to the specified vector. The resultant vector will have the same magnitude as the source vector, and their scalar product will be zero. The direction of the return vector will equal Vec2Ang(Vec) - 90.

```pascal
FUNCTION Perp(Vec : VECTOR): VECTOR;
```

```python
def vs.Perp(Vec):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Vec|VECTOR|Source vector.|

## Remarks
(*\_c\_*, 2022.01.19) In VS Python the tuple returned is always 3-dimensional, but the third value is always zero (see comment below for VS Pascal). So this is a 2D only routine.

(\_c\_, 2011.01.25) The z-value of the vector returned by Perp is always zero. If your source vector has z<>0 the resulting vector might not be what you expect, because of the source vector's angle.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    v1, v2 : VECTOR;
BEGIN
    v1.x := 12; v1.y := 1;
    v2.x := 3; v2.y := 15;
    Message( Perp(v1-v2) );
END;
Run(Example);
```
#### Python ####
```python
v1 = (12, 1, 0) # 3-dimensional tuple. Perp accepts also a 2-dimensional tuple
v2 = (3, 15, 0)
vs.Message( str(vs.Perp (v1[0] - v2[0], v1[1] - v2[1], v1[2] - v2[2]) )) )
```

```pascal
GetUnits(fraction, display, format, upi, name, sqName);
halfFont := kHalfFont * upi * GetLScale(ActLayer);
tmpAngle := Vec2Ang(segVector);
tmpVector := 0.5*segVector;
labelVector := -1 * Perp(UnitVec(tmpVector)) * halfFont;

IF ( startAng + sweepAng/2 > 360 ) THEN semiSweepAng := startAng + sweepAng/2 - 360
	ELSE semiSweepAng := startAng + sweepAng/2 ;
vec1 := Ang2Vec( semiSweepAng, Radius ) + cen_pt;
{calculate the tangent to the Arc in the vec1 point }
vec2 := Perp( vec1 - cen_pt ) + vec1;
{calculate the left and right bisector Line of the Arc semi-Angle from Arc center to the Arc Line}
IF ( startAng + sweepAng/4 > 360 ) THEN semiSweepAng := startAng + sweepAng/4 - 360
	ELSE semiSweepAng := startAng + sweepAng/4 ;
vecA := Ang2Vec( semiSweepAng, Radius ) + cen_pt;

BEGIN
	pt2 := pt1 + ((pt5 - pt1) / 3)     + (Perp(pt5 - pt1) / 30);
	pt4 := pt1 + ((pt5 - pt1) / 3 * 2) - (Perp(pt5 - pt1) / 30);
END ELSE BEGIN
	pt2.x := pControlPoint01X;
	pt2.y := pControlPoint01Y;
```
```python
import vs

# Returns a vector which is perpendicular to the specified vector.
Vec = (0, 0)

vec = vs.Perp(Vec)
vs.Message('Perp returned: ' + str(vec))
```

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
