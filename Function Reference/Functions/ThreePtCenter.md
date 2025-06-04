# ThreePtCenter

## Description
Returns the center of a circle passing thru 3 given points.

```pascal
FUNCTION ThreePtCenter(
				pt1 : VECTOR;
				pt2 : VECTOR;
				pt3 : VECTOR): VECTOR;
```

```python
def vs.ThreePtCenter(pt1, pt2, pt3):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt1|VECTOR|   |
|pt2|VECTOR|   |
|pt3|VECTOR|   |

## Remarks
([[User:CBM-c-|_c_]], 2022.01.18) In VS Python this routine returns a 3-dimensional tuple. Warning: Most Math - Vector routines require a 3-dimensional tuple, failing to init a third item in VW before 2023 (vs.Vec2Ang, for example, returns gibberish on 2-d tuples).

## Examples
==== VectorScript ====
```pascal
{ finds the tangent angle between two poly sides }
PROCEDURE Example;
VAR
    polyObj : HANDLE;
    p1, p2, p3, c, t : VECTOR;
    ang : REAL;

BEGIN
polyObj := FSActLayer; { take care to have a polygon selected }
IF polyObj <> NIL THEN BEGIN { not checking here for obj type, but you should }
    GetPolyPt( polyObj, 1, p1.x, p1.y );
    GetPolyPt( polyObj, 2, p2.x, p2.y );
    GetPolyPt( polyObj, 3, p3.x, p3.y );

    c := ThreePtCenter( p1, p2, p3 );
    Locus( c.x, c.y );

    t := Perp( p2 - c );
    ang := Vec2Ang( t );
    AlrtDialog( Concat('Angle of tangent at pt2: ', Chr(13), Num2Str(3, ang)) ); 
END;
Run(Example);
```
==== Python ====
```python
# finds the tangent angle between two poly sides
polyObj = vs.FSActLayer() # take care to have a polygon selected
if polyObj != vs.Handle( 0 ): # not checking here for obj type, but you should
    p1 = vs.GetPolyPt( polyObj, 1 ) 
    p2 = vs.GetPolyPt( polyObj, 2 )
    p3 = vs.GetPolyPt( polyObj, 3 ) 

    c = vs.ThreePtCenter( p1, p2, p3 )
    vs.Locus( c )

    t = vs.Perp( p2[0] - c[0], p2[1] - c[1], 0 ) 
    ang = vs.Vec2Ang( t )
    vs.AlrtDialog( f'Angle of tangent at pt2:\r{ang:.3f}' ) # precision = 3, coercing float
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
