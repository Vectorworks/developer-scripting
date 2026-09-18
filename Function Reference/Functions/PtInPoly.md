# PtInPoly

## Description
Function PtInPoly returns TRUE if the point specified point lies within, or on, the referenced polygon or polyline object.

```pascal
FUNCTION PtInPoly(
				pX,pY : REAL;
				h     : HANDLE): BOOLEAN;
```

```python
def vs.PtInPoly(p, h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|X-Y coordinate point.|
|h|HANDLE|Handle to polygon.|

## Remarks
(\_c\_ 2021.12.27): This only works on polygons or segments of polylines whose vertex type is corner. Any point on poly segments with other vertex type (bezier, arc, radius, cubic) will return false. Also small polygon sides will cause failure. All in all it is barely usable for anything than large polygons (not polylines) with large sides.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
polyHandle :HANDLE;
locusHandle :HANDLE;
x, y :REAL;
BEGIN
CallTool(-204); polyHandle := FSActLayer;
CallTool(-221); locusHandle := FSActLayer;
GetLocPt(locusHandle, x, y);
Message(PtInPoly(x, y, polyHandle));
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
{Determine if a leader line from poly to tag is necessary and draw if so.}
Polyline2ARRAY(pathHandle, 359, .1, FALSE, FALSE, vertices, vertex_cnt);
if PtInPoly(X, Y, gPolyHandle) then BEGIN
	GetFillBack(objHand, r, g, b);
end else BEGIN
	ColorIndexToRGB(0, r, g, b);
	pt.x := x;
	pt.y := y;

	IF gAllowSeatPastBound THEN
		IsSymbolInsidePoly := PtInPoly( seatPt.x, seatPt.y, pathHand )
	ELSE
		IsSymbolInsidePoly := ( PtInPoly( p1X, p1Y, pathHand ) & PtInPoly( p2X, p2Y, pathHand )
								& PtInPoly( p2X, p1Y, pathHand ) & PtInPoly( p1X, p2Y, pathHand ) );
END;

IF dir_uv.x = -1 THEN BubbleVector(sects, 1, 'descending', sect_cnt);
FOR cnt1 := 1 TO sect_cnt - 1 DO BEGIN
	mid_pt := (sects[cnt1] + sects[cnt1 + 1]) / 2;
	IF ((GetType(poly_h) = 3) & PtInRect(mid_pt.x, mid_pt.y, verts[1,1], verts[1,2], verts[3,1], verts[3,2])) |
		PtInPoly(mid_pt.x, mid_pt.y, poly_h)
	THEN BEGIN
		OK := TRUE;
		FOR cnt2 := 1 TO holes_cnt DO BEGIN
			IF PtInPoly(mid_pt.x, mid_pt.y, holes[cnt2].h) THEN BEGIN
				OK := FALSE;
				cnt2 := holes_cnt;
```
```python
result = vs.PtInPoly((0, 0), h)
```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
