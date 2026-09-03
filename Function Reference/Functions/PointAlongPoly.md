# PointAlongPoly

## Description
Returns a point at the specified distance along the poly, and a vector tangent to the poly at that point.

```pascal
FUNCTION PointAlongPoly(
				h           : HANDLE;
				dist        : REAL;
				VAR pt      : VECTOR;
				VAR tangent : VECTOR): BOOLEAN;
```

```python
def vs.PointAlongPoly(h, dist):
    return (BOOLEAN, pt, tangent)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|dist|REAL|   |
|pt|VECTOR|   |
|tangent|VECTOR|   |

## Remarks
(\_c\_, 2022.01.18) In Vectorscript Python this returns a tuple with 3 items ( 0, 0, 0 ). This is relevant for usage in routines such as [Vec2Ang](Vec2Ang.md), returning wrong values if the tuple is only bidimensional.

## Examples
==== Pascal ====
```pascal
PROCEDURE Test;
VAR
    polyObj : HANDLE;
    dist : REAL;
    p, tangentVec : VECTOR;
	
BEGIN
    polyObj := FSActLayer;

    IF polyObj = NIL THEN
        AlrtDialog( 'Select a polygon' )
		
    ELSE BEGIN
        dist := 1m;
        IF PointAlongPoly( polyObj, dist, p, tangentVec ) THEN
            Locus( p.x, p.y );
    END;
END;
Run(Test);
```
#### Python ####
```python
def Str2Num( inStr ):
    ok, num = vs.ValidNumStr( inStr )
    if ok:
        return num
    else:
        return 0

polyObj = vs.FSActLayer()

if polyObj == vs.Handle():
    vs.AlrtDialog( 'Select a polygon' )
else:
    dist = Str2Num( '1m' ) # convert string to dim
    ok, p, tangentVec = vs.PointAlongPoly( polyObj, dist )
    if ok:
        vs.Locus( p )
        vs.AlrtDialog( str( len(p)) ) # return a tuple with 3 items
```

```pascal
BEGIN
temp_b := PointAlongPoly(basepoly_h,(temp_i*spacing),pt,tangent);
basepoints[temp_i] := pt;
tmp1_v := tangent;
tmp1_v := ang2vec(vec2ang(tmp1_v)+90,-corru_ht);
ctrpoints[temp_i] := basepoints[temp_i] + tmp1_v;

BEGIN
			BSB := PointAlongPoly(TempH,gFirstPitch/2,cen_pt,TanVec);
BSB := PointAlongPoly(TempH,gSymPitch/2,LastPoint,TanVec);
SegAng := Vec2Ang(TanVec);
			IF gUseVertPitch THEN SegAng := SegAng+90;
GetPolyPt(TempH,1,pX, pY);

BEGIN
{Set the Elevation marker to the center of the line.}
IF PointAlongPoly(hPathObj,HPerim(hPathObj)/2,V1,v2) THEN
	BEGIN
	gElevationLoc.X := v1.x;
	gElevationLoc.Y := v1.y;
	IF gConfig = ksElevation THEN
		BEGIN
		gTextLoc.X := v1.x;
```
```python
import vs

# Returns a point at the specified distance along the poly, and a vector
# tangent to the poly at that point.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
dist = 1.0

ok, pt, tangent = vs.PointAlongPoly(h, dist)
vs.Message('PointAlongPoly returned: ' + str((ok, pt, tangent)))
```

## See Also
VS Functions:
* [PointAlongPolyN](PointAlongPolyN.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
