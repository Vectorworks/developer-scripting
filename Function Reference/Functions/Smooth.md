# Smooth

## Description
Procedure Smooth sets the smoothing type of newly created polyline or polygon objects.

**Table - Smoothing Types**

| Smooth Type | Constant |
|-------------|----------|
| None        | 0        |
| Bezier      | 1        |
| Cubic       | 2        |
| Arc         | 3        |

```pascal
PROCEDURE Smooth(smoothType : INTEGER);
```

```python
def vs.Smooth(smoothType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|smoothType|INTEGER|Smoothing style.|

## Examples
#### VectorScript ####
```pascal
Smooth(2);
Poly(0, 0, -0.5, 1, 0.5, 2);
```
#### Python ####
```python

```

```pascal
{ set cubic smoothing for curved flights. }
IF bCurvedFlight THEN Smooth( 2 ); { cubic smoothing. }

theRadius := kHeadRadius * upi * gScaleFactor;
Oval( -theRadius, theRadius, theRadius, -theRadius );
SetFPat( LNewObj, 1 );
OpenPoly;
Smooth( 1 );
BeginPoly;
	AddPoint( theRadius,0);
	AddPoint( gControlArcPt[1], gControlArcPt[2] );
	AddPoint( gControlEndPt[1], gControlEndPt[2] );

GetSegPt1( lineHandle, x1, y1 );
GetSegPt2( lineHandle, x2, y2);
OpenPoly;
FillPat( 0 );
Smooth( gCornerType );
BeginPoly;
MakeFuzzyLineSegment( x1, y1, x2, y2 );
```
```python
vs.Smooth(smoothType)
```

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
