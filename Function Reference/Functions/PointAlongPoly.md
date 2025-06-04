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
([[User:CBM-c-| _c_]], 2022.01.18) In Vectorscript Python this returns a tuple with 3 items ( 0, 0, 0 ). This is relevant for usage in routines such as [[VS:Vec2Ang | Vec2Ang]], returning wrong values if the tuple is only bidimensional.

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
==== Python ====
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

## See Also
VS Functions:
* [PointAlongPolyN](PointAlongPolyN.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
