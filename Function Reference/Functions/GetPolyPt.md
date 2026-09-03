# GetPolyPt

## Description
Procedure GetPolyPt returns the coordinates of a specified vertex of the referenced object.

```pascal
PROCEDURE GetPolyPt(
				objectHd  : HANDLE;
				index     : INTEGER;
				VAR pX,pY : REAL);
```

```python
def vs.GetPolyPt(objectHd, index):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to polygon.|
|index|INTEGER|Index of vertex (range of 1 to n).|
|p|REAL|Returns coordinates of vertex.|

## Remarks
(*\_c\_*, 2022.01.18) In VS Python this routine returns a 2-dimensional tuple. Warning: Most Math - Vector routines require a 3-dimensional tuple, failing to init a third item in VW before 2023 (vs.Vec2Ang, for example, returns gibberish on 2-d tuples). You will need to make sure that a third item exists.
```python
# test GetPolyPt
p = (0, 0, 0)
vs.AlrtDialog( 'init tuple: ' + str(len(p)) ) # 3 items
p = vs.GetPolyPt(vs.FSActLayer(), 1) # take care to have a polygon selected
vs.AlrtDialog( 'after GetPolyPt: ' + str(len(p)) ) # 2 items?!?
```

(*\_c\_*, 2010.12.22) Since the introduction of rotated rectangles, it doesn't turn them into polygons any longer. The routine fails with warning, as expected. 

(Charles Chandler, 2001 Jan. 25): Doesn't work on rectangles, unless you rotate them, which turns them into polygons.

## Examples
#### VectorScript ####
```pascal
FOR i := 1 to GetVertNum(thePoly) DO
    GetPolyPt(thePoly, i, vertX, vertY);
```
#### Python ####
```python
def Example():
    obj = vs.FSActLayer()
    for vertexNum in range(1, vs.GetVertNum(obj)):
        ptVt = vs.GetPolyPt(obj, vertexNum)
        vs.TextOrigin(ptVt[0], ptVt[1])
        vs.CreateText(vs.Concat('vNum: ', vertexNum))
Example()
```

```pascal
BEGIN
	GetPolyPt(lineHandle, vertexNum, x, y);
	MoveTo(x, y);

for cnt1 := 1 to wall_cnt do BEGIN
	IF doGross THEN BEGIN
		h1 := OffsetPolygon(walls[cnt1], -1");
		for cnt2 := GetVertNum(h1) downto 2 do BEGIN
			GetPolyPt(h1, cnt2 - 1, pt1.x, pt1.y);
			GetPolyPt(h1, cnt2,     pt2.x, pt2.y);
			IF Abs(Norm(pt2 - pt1)) < .0625" THEN DelVertex(h1, cnt2);
		END;

BEGIN
	Perim := 0;
	FOR j := 1 TO GetVertNum (hPoly) DO BEGIN
		GetPolyPt (hPoly, j, x2, y2);
		IF j = 1 THEN BEGIN
			x0 := x2;
			y0 := y2;
		END
```
```python
import vs

# Procedure GetPolyPt returns the coordinates of a specified vertex of the
# referenced object.
objectHd = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

result = vs.GetPolyPt(objectHd, index)
```
See also in tutorials: [15. Uniform Arc-Length Resampling of a Polyline](ai%20examples/15_PolylineResampleUniform.md), [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md)

## See Also
For polygons:
* [SetPolyPt](SetPolyPt.md)

For polylines:
* [GetPolylineVertex](GetPolylineVertex.md)
* [SetPolylineVertex](SetPolylineVertex.md)

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
