# Vec2Ang

## Description
Returns the angle, in degrees, of the specified vector. If Vect is a 3D vector, Vec2Ang will return the 3D angle between Vect and the X axis. If Vect is {0,0,0}, Vec2Ang returns -90.

```pascal
FUNCTION Vec2Ang(Vect : VECTOR): REAL;
```

```python
def vs.Vec2Ang(Vect):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Vect|VECTOR|Source vector.|

## Remarks
(\_c\_, 2022.01.18) For Vectorscript Python you might need to add a third item in the tuple for the vector, or vs.Vec2Ang will return 90/-90. This is the opposite in VS Pascal.

## Examples
#### VectorScript ####
```pascal
{ ... }
p : VECTOR;
vtx1 : INTEGER;
{ ... }

{ fetches coordinates of vertex 1 in a polygon, remember to use GetPolylineVertex if it's a polyline!  }
vtx1 := 1;
GetPolyPt( polyHandle, vtx1, p.x, p.y ); 

ang := Vec2Ang( p );
```
#### Python ####
```python
p = vs.GetPolyPt( polyHandle, vtx1 ) # sets a tuple with 2 items in the form ( 0, 0 )
ang = vs.Vec2Ang( (p[0], p[1], 0) ) 
# make sure that there is a z coordinate or vs.Vec2Ang will fail, if p has only 2 items (VS Python only, Pascal OK )

# alternatively

if len(p) == 2:
    p += (0,) # add a 3rd item to the tuple
ang = vs.Vec2Ang( p ) # returns angle

# FAILURE EXAMPLES:
# ang = vs.Vec2Ang( p ) # always returns 90
# ang = vs.Vec2Ang( (p[0], p[1]) ) # always returns 90
```

```pascal
BEGIN
	theRadius    := Norm(ptA - centerPt);
	theAngle     := Vec2Ang(ptA - centerPt);
	theArcLength := LenOfArc(centerPt, ptA, ptB);
	theta        := AngBVec(ptA-centerPt, ptB-centerPt);
	chord        := Sin(Deg2Rad(Abs(theta/2))) * theRadius * 2;
	T            := theRadius * Tan(Deg2Rad(theta/2));

v1 [1] := x1;	v1 [2] := y1;	v1 [3] := 0;
v2 [1] := x2;	v2 [2] := y2;	v2 [3] := 0;
v3 := v2 - v1;
IF isCircle THEN beta := 0
ELSE beta := Vec2Ang (v3);

{calc the object rotation}
rotCN := Vec2Ang( endCNV - startCNV );
```
```python
import vs

# Returns the angle, in degrees, of the specified vector.
Vect = (0, 0)

value = vs.Vec2Ang(Vect)
vs.Message('Vec2Ang returned: ' + str(value))
```
See also in tutorials: [11. 2D Vector Math Toolkit](ai%20examples/11_VectorMathToolkit.md)

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
