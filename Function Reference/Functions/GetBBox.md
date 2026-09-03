# GetBBox

## Description
Procedure GetBBox returns the bounding box of the projection of the referenced object on the screen plane.

```pascal
PROCEDURE GetBBox(
				h           : HANDLE;
				VAR p1X,p1Y : REAL;
				VAR p2X,p2Y : REAL);
```

```python
def vs.GetBBox(h):
    return (p1, p2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|p1|REAL|Top left coordinate of bounding box.|
|p2|REAL|Bottom right coordinate of bounding box.|

## Remarks
*\_c\_*, 2017.02.24: GetBBox fails unpredictably on Roof faces when in top-plan: it returns a bounding box dependent on the axis widget and the page position of the face. Avoid the axis widget setting the view to Top, then the returned values will be correct. This is valid up to VW 2017 (bug reported).

## Examples
```pascal
BEGIN
	dCL := kCL;
	GetBBox( LNewObj, xb1, yb1, xb2, yb2 );

{determine the coords of the real bounding box segment on the side of the Group, which is always the side of the text origin}
realBBV1 := Ang2Vec( 90+ang , 1);
realBBV1 := realBBV1 + originVec;
{Get the reported by VW BoundingBox ot the rotated TextBlock}
GetBBox( textH, BBVec1[1], BBVec1[2], BBVec2[1], BBVec2[2] );
{check where each of the real bbox segments intersects with the calculated one in order to find its satrt and end coords}
found1 := FALSE; found2 := FALSE;
tempV[1] := BBVec2[1]; tempV[2] := BBVec1[2];
if IntersLineLine( originVec, realBBV1, BBVec1, tempV, intersV ) then BEGIN

VSave ('__SeatingLayoutTempView');
SetView (0, 0, 0, 0, 0, 0);
Symbol(symName, 0, 0, 0);
h := LNewObj;
GetBBox(h, p1x, p1y, p2x, p2y);
gRowSpacing := Str2Num(GetRField(objHand, kSeatingObjectName, 'RowSpacing'));
gSeatSpacing := Str2Num(GetRField(objHand, kSeatingObjectName, 'SeatSpacing'));
SeatSpacing := p2x - p1x;
RowSpacing := p1y - p2y;
```
```python
if( vs.GetPref( kBoundsSettingDisable ) ):
	vs.SetPref( kBoundsSettingDisable, False )
	vs.ResetObject( hMarkerHand )
	pt1,pt2 = vs.GetBBox( hMarkerHand )
	vs.SetPref( kBoundsSettingDisable, True )

vs.SetTextJust( vs.LNewObj(), 2 )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 0 )
b1, b2 = vs.GetBBox( vs.LNewObj() )
vs.Rect( kBf * b1[0], kBf * b1[1], kBf * b2[0], kBf * b2[1] )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 1 )
vs.HMoveBackward( vs.LNewObj(), False )
```
See also in tutorials: [10. Iterate the Drawing and Report a Summary](ai%20examples/10_IterateAndReport.md), [13. Point-in-Polygon Test (Ray Casting)](ai%20examples/13_PointInPolygonRayCast.md)

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
