# CrossProduct

## Description
Returns the cross product of the two specified vectors.

The cross product is also known as the vector product of the two vectors. The result is a vector whose magnitude is equivalent to the product of the magnitudes of the two vectors multiplied by the sine of the smaller angle between the two vectors. The direction of the resultant vector is perpendicular to a plane formed by the two source vectors.

```pascal
FUNCTION CrossProduct(
				v1 : VECTOR;
				v2 : VECTOR): VECTOR;
```

```python
def vs.CrossProduct(v1, v2):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v1|VECTOR|Source vector 1.|
|v2|VECTOR|Source vector 2.|

## Remarks
(*\_c\_*, 2022.01.20) The vector returned is always 3-dimensional: Pascal: vector {x, y, z}, Python: tuple (0.0, 0.0, 0.0).
Note: in Python the two vectors used as parameters MUST be 3-dimensional, or it will return gibberish for the x, y values. This doesn't matter in Pascal.

```python
# EXAMPLE OF FAULTY USAGE
v1 = (12, 1) # bidimensional
v2 = (3, 15) 
vs.Message( str(vs.CrossProduct(v1, v2)) ) 
# returns gibberish for first two items
```

[[User:Ptr|Ptr]] [2021.05.12]:
Since in Python a VECTOR doesn't exist, you need to use tuples instead.

''' older posts whose author got lost:'''

This is provided for cross-platform compatibility.

To elaborate a little...
The first vector defines the X axis of a new coordinate system; the second vector defines the positive Y direction in that coordinate system. The cross product of those vectors will be in the positive Z direction.

## Examples
#### VectorScript ####
```pascal
PROCEDURE TEST;
VAR
    v1, v2 : VECTOR;

BEGIN
    v1.x := 12; v1.y := 1; v1.z := 0;
    v2.x := 3; v2.y := 15; v2.z := 0;
    Message( CrossProduct(v1, v2)); { returns a 3-dimensional VECTOR }
END;
Run(TEST);
```
#### Python ####
```python
v1 = (12, 1, 0)
v2 = (3, 15, 0)
vs.Message( str(vs.CrossProduct(v1, v2)) ) # returns a 3-dimensional tuple
```

```pascal
vVec := CrossProduct( uVec, wVec );
{old}
{ Create3DCurveAt( uVec, vVec, wVec, pt1 ); }

segInitComplete := TRUE;
FOR i := 1 TO insidePts_cnt DO BEGIN
	IF PointBtwLines(insidePts[i], seg, centerSeg) THEN BEGIN
		segInitComplete := FALSE;
		temp_v := CrossProduct(insidePts[i]-bound1[1], bound1[2]-bound1[1]);
		IF PointBtwLines(insidePts[i], bound1, midAxis) | Eq( temp_v.z, 0, 0.001" ) THEN BEGIN
				seg[1] := insidePts[i];
		END ELSE BEGIN
				seg[2] := insidePts[i];

				END;
		END;
	END;
vec_ang := angbvec(v1,v2);
xp := crossproduct(v1,v2);
xp := unitvec(xp);
isCW := GetObjectVariableBoolean(poly_h,652);
IsVert2DConcave := ((isCW & (xp = vRef)) | (NOT(isCW) & (xp <> vRef)));
END;
```
```python
import vs

# Returns the cross product of the two specified vectors.
v1 = (0, 0)
v2 = (1, 1)

vec = vs.CrossProduct(v1, v2)
vs.Message('CrossProduct returned: ' + str(vec))
```

## Version
Availability: from VectorWorks 8.5

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
